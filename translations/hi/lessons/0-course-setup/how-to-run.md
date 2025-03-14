# कोड कैसे चलाएं

इस पाठ्यक्रम में बहुत सारे निष्पादन योग्य उदाहरण और प्रयोगशालाएं शामिल हैं जिन्हें आप चलाना चाहेंगे। ऐसा करने के लिए, आपको इस पाठ्यक्रम के हिस्से के रूप में प्रदान किए गए Jupyter Notebooks में Python कोड चलाने की क्षमता की आवश्यकता है। कोड चलाने के लिए आपके पास कई विकल्प हैं:

## अपने कंप्यूटर पर स्थानीय रूप से चलाना

अपने कंप्यूटर पर स्थानीय रूप से कोड चलाने के लिए, आपको Python का कोई संस्करण स्थापित करना होगा। मैं व्यक्तिगत रूप से **[miniconda](https://conda.io/en/latest/miniconda.html)** स्थापित करने की सिफारिश करता हूं - यह एक हल्का इंस्टॉलेशन है जो विभिन्न Python **वर्चुअल वातावरणों** के लिए `conda` पैकेज प्रबंधक का समर्थन करता है।

जब आप miniconda स्थापित कर लें, तो आपको रिपॉजिटरी क्लोन करनी होगी और इस पाठ्यक्रम के लिए उपयोग किए जाने वाले वर्चुअल वातावरण को बनाना होगा:

```bash
git clone http://github.com/microsoft/ai-for-beginners
cd ai-for-beginners
conda env create --name ai4beg --file .devcontainer/environment.yml
conda activate ai4beg
```

### Python एक्सटेंशन के साथ Visual Studio Code का उपयोग करना

पाठ्यक्रम का उपयोग करने का सबसे अच्छा तरीका इसे [Visual Studio Code](http://code.visualstudio.com/?WT.mc_id=academic-77998-cacaste) में [Python Extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python&WT.mc_id=academic-77998-cacaste) में खोलना है।

> **Note**: जब आप क्लोन करते हैं और VS Code में निर्देशिका खोलते हैं, तो यह स्वचालित रूप से आपको Python एक्सटेंशन स्थापित करने का सुझाव देगा। आपको ऊपर बताए अनुसार miniconda भी स्थापित करना होगा।

> **Note**: यदि VS Code आपको कंटेनर में रिपॉजिटरी को फिर से खोलने का सुझाव देता है, तो आपको स्थानीय Python इंस्टॉलेशन का उपयोग करने के लिए इसे अस्वीकार करना होगा।

### ब्राउज़र में Jupyter का उपयोग करना

आप अपने कंप्यूटर पर ब्राउज़र से सीधे Jupyter वातावरण का भी उपयोग कर सकते हैं। वास्तव में, पारंपरिक Jupyter और Jupyter Hub दोनों स्वचालित पूर्णता, कोड हाइलाइटिंग आदि के साथ एक बहुत सुविधाजनक विकास वातावरण प्रदान करते हैं।

स्थानीय रूप से Jupyter शुरू करने के लिए, पाठ्यक्रम की निर्देशिका पर जाएं, और निष्पादित करें:

```bash
jupyter notebook
```
या
```bash
jupyterhub
```
इसके बाद आप किसी भी `.ipynb` files, open them and start working.

### Running in container

One alternative to Python installation would be to run the code in container. Since our repository contains special `.devcontainer` फ़ोल्डर में जा सकते हैं जो इस रिपॉजिटरी के लिए कंटेनर बनाने के निर्देश देता है, VS Code आपको कोड को कंटेनर में फिर से खोलने का प्रस्ताव देगा। इसके लिए Docker इंस्टॉलेशन की आवश्यकता होगी, और यह अधिक जटिल भी होगा, इसलिए हम इसे अधिक अनुभवी उपयोगकर्ताओं के लिए सिफारिश करते हैं।

## क्लाउड में चलाना

यदि आप स्थानीय रूप से Python स्थापित नहीं करना चाहते हैं, और आपके पास कुछ क्लाउड संसाधनों तक पहुंच है - तो कोड को क्लाउड में चलाने का एक अच्छा विकल्प होगा। आप इसे करने के कई तरीके हैं:

* **[GitHub Codespaces](https://github.com/features/codespaces)** का उपयोग करना, जो आपके लिए GitHub पर बनाया गया एक वर्चुअल वातावरण है, जिसे VS Code ब्राउज़र इंटरफ़ेस के माध्यम से एक्सेस किया जा सकता है। यदि आपके पास Codespaces तक पहुंच है, तो आप बस रिपॉजिटरी में **Code** बटन पर क्लिक कर सकते हैं, एक कोडस्पेस शुरू कर सकते हैं, और बिना समय बर्बाद किए चलना शुरू कर सकते हैं।
* **[Binder](https://mybinder.org/v2/gh/microsoft/ai-for-beginners/HEAD)** का उपयोग करना। [Binder](https://mybinder.org) एक मुफ्त कंप्यूटिंग संसाधन है जो क्लाउड में लोगों को GitHub पर कुछ कोड का परीक्षण करने के लिए प्रदान किया गया है। मुख्य पृष्ठ पर एक बटन है जो रिपॉजिटरी को Binder में खोलता है - यह आपको तेजी से बाइंडर साइट पर ले जाएगा, जो अंतर्निहित कंटेनर बनाएगा और आपके लिए Jupyter वेब इंटरफ़ेस शुरू करेगा।

> **Note**: दुरुपयोग को रोकने के लिए, Binder को कुछ वेब संसाधनों तक पहुंच अवरुद्ध है। इससे कुछ कोड काम करने में रुकावट आ सकती है, जो सार्वजनिक इंटरनेट से मॉडल और/या डेटासेट लाते हैं। आपको कुछ समाधान खोजने की आवश्यकता हो सकती है। इसके अलावा, Binder द्वारा प्रदान किए गए कंप्यूट संसाधन काफी बुनियादी हैं, इसलिए प्रशिक्षण धीमा होगा, विशेष रूप से बाद के अधिक जटिल पाठों में।

## GPU के साथ क्लाउड में चलाना

इस पाठ्यक्रम के कुछ बाद के पाठ GPU समर्थन से बहुत लाभान्वित होंगे, क्योंकि अन्यथा प्रशिक्षण बहुत धीमा होगा। आपके पास कुछ विकल्प हैं, विशेष रूप से यदि आपके पास [Azure for Students](https://azure.microsoft.com/free/students/?WT.mc_id=academic-77998-cacaste) के माध्यम से या अपने संस्थान के माध्यम से क्लाउड तक पहुंच है:

* [Data Science Virtual Machine](https://docs.microsoft.com/learn/modules/intro-to-azure-data-science-virtual-machine/?WT.mc_id=academic-77998-cacaste) बनाएं और Jupyter के माध्यम से इससे कनेक्ट करें। आप फिर मशीन पर सीधे रिपॉजिटरी क्लोन कर सकते हैं, और सीखना शुरू कर सकते हैं। NC-सीरीज VMs में GPU समर्थन है।

> **Note**: कुछ सब्सक्रिप्शन, जिसमें Azure for Students शामिल है, बिना किसी अतिरिक्त सेटअप के GPU समर्थन प्रदान नहीं करते हैं। आपको तकनीकी सहायता अनुरोध के माध्यम से अतिरिक्त GPU कोर का अनुरोध करने की आवश्यकता हो सकती है।

* [Azure Machine Learning Workspace](https://azure.microsoft.com/services/machine-learning/?WT.mc_id=academic-77998-cacaste) बनाएं और फिर वहां नोटबुक फीचर का उपयोग करें। [यह वीडियो](https://azure-for-academics.github.io/quickstart/azureml-papers/) दिखाता है कि Azure ML नोटबुक में रिपॉजिटरी को कैसे क्लोन करें और इसका उपयोग करना शुरू करें।

आप Google Colab का भी उपयोग कर सकते हैं, जो कुछ मुफ्त GPU समर्थन के साथ आता है, और वहां Jupyter Notebooks अपलोड कर सकते हैं ताकि उन्हें एक-एक करके निष्पादित किया जा सके।

**अस्वीकृति**:  
यह दस्तावेज़ मशीन-आधारित एआई अनुवाद सेवाओं का उपयोग करके अनुवादित किया गया है। जबकि हम सटीकता के लिए प्रयासरत हैं, कृपया ध्यान दें कि स्वचालित अनुवादों में त्रुटियाँ या असत्यताएँ हो सकती हैं। मूल दस्तावेज़ को उसकी मूल भाषा में प्राधिकृत स्रोत माना जाना चाहिए। महत्वपूर्ण जानकारी के लिए, पेशेवर मानव अनुवाद की सिफारिश की जाती है। हम इस अनुवाद के उपयोग से उत्पन्न किसी भी गलतफहमी या गलत व्याख्या के लिए जिम्मेदार नहीं हैं।
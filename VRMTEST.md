*Quick links :*
[Coffee](README.md) - [Watson Studio](STUDIO.md) - [Visual Recognition Model](VISRECO.md) - [**Test and Deploy**](VRMTEST.md)
***

## Lab Objectives

In this lab you will use sample images to confirm your Visual Recognition model. You will learn:

- How to test your Visual Recognition model using sample images
- How to incorporate your Visual Recognition Custom Classifier model into your applications

#### Review and Test
- Review the Classes and Model details
- Click on the **Test** tab

![Watson Studio  screenshot](screenshots/WatsonStudio-VisualRecognitionModelSummary.png)

### Test Watson Visual Recognition Custom Classifier with sample images
- Visit the [Test Data directory](testdata) and **download** the testdata.zip file.  This zip file contains PNG and JPG images
- Unlike the training datasets, you will need to **unzip** the images onto your local hard drive
- Inspect a few of the breakfast images using a local image viewing utility or file browser
- These images were not part of the training set and will be used to validate the visual recognition model
- Return to the **Test** tab in the Watson Studio Flooding project
- There are two techniques to upload the images into the **Test** page
  - Drag the individual images from your local file browser into the Test page
  - Click on the **browse** link to open a file selection dialog

![Watson Studio  screenshot](screenshots/WatsonStudio-VisualRecognitionModelTestBlank.png)

- The trained custom classifier model will analyze the images
- Inspect the **Confidence scores** returned by the Watson Visual Recognition Custom Classifier

![Watson Studio  screenshot](screenshots/WatsonStudio-VisualRecognitionModelTestResults.png)

### Implement Watson Visual Recognition custom model in your Applications
- You can incorporate this Watson Visual Recognition Custom Classifier model into your applications using a variety of programming languages - Java, Node, Python, Ruby, Core ML
- Click on the **Implementation** tab to review the Code snippets

![Watson Studio  screenshot](screenshots/WatsonStudio-VisualRecognitionModelImplement.png)

Use the code snippets below to classify images against your model. For reference, the full API specification is available [here](https://www.ibm.com/watson/developercloud/visual-recognition/api/v3/)

In the IBM Cloud Dashboard, search for and open your instance of *Watson Visual Recognition* and navigate into the Service Credentials section. Copy your **apikey** for use in the curl examples below.

- **API endpoint**

  ```
  https://gateway.watsonplatform.net/visual-recognition/api
  ```

- **Authentication**

  ```
  curl -u "apikey:{apikey}" "https://gateway.watsonplatform.net/visual-recognition/api/{method}"
  ```

- **Classify an image (GET)**

  ```
  curl -u "apikey:{apikey}" "https://gateway.watsonplatform.net/visual-recognition/api/v3/classify?url=https://watson-developer-cloud.github.io/doc-tutorial-downloads/visual-recognition/fruitbowl.jpg&version=2018-03-19&classifier_ids=CofCoffeeorDonuts_418020421"
  ```

- **Classify an image (POST)**

  ```
  curl -X POST -u "apikey:{apikey}"-F "images_file=@fruitbowl.jpg" -F "threshold=0.6" -F "classifier_ids=CoffeeorDonuts_418020421" "https://gateway.watsonplatform.net/visual-recognition/api/v3/classify?version=2018-03-19"
  ```

### Congratulations
  You have completed the Coffee or Donuts Visual Recognition Lab and have identified Coffee Bags, Coffee Mugs and yummy donuts.

### Visual Recognition - Additional References
- [Call for Code Visual Recognition](https://developer.ibm.com/callforcode/resources/visual-recognition/)
- [Locate and count items with object detection](https://developer.ibm.com/code/patterns/locate-and-count-items-with-object-detection/)
- [MAX Object Detection](https://developer.ibm.com/exchanges/models/all/max-object-detector/)

*Quick links :*
[Coffee](README.md) - [Watson Studio](STUDIO.md) - [Visual Recognition Model](VISRECO.md) - [**Test and Deploy**](VRMTEST.md)

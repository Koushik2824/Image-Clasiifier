# Image-Clasiifier
This is a web app built using streamlit  
[Link to Web app
](https://imagea.streamlit.app/)  
## Steps:
1.Webscraping using Selenium,a python library  
2.Convolutional Neural Network Model building and training  
3.Saving the model and creating a webapp using streamlit


**PART-1::**
  **WEB SCRAPING**(DONE BY HIMANGSHU DEKA)
  1. FIRST CREATED A CHROME DRIVER INSTANCE 
<img width="1022" alt="Screenshot 0005-07-29 at 14 28 49" src="https://github.com/KewangZhili/Image_Clasiifier/assets/111041497/add17153-79b7-4ce2-afef-d4a13d7e8f97">
  2. THEN WROTE A FUNCTION THAT TAKES IN URL AND NO. OF IMAGES TO BE DOWNLOADED, AND DOWNLOADS THE IMAGES FROM THE SAID URL INTO A FILE CREATED USING THE FUNCTIONS AS DEPICTED BELOW::


<img width="996" alt="Screenshot 0005-07-29 at 14 29 59" src="https://github.com/KewangZhili/Image_Clasiifier/assets/111041497/a8a930e6-1043-496b-af1b-fb444fd770c3">

3. HERE NOTE THAT WE ARE EXCLUDING EVERY 25TH IMAGE, THIS IS BECAUSE::AS WE CLICK AN IMAGE IN GOOGLE IMAGES EVERY 25TH INDEXED ELEMENT IS INSTEAD A LINK THAT STANDS FOR "VIEW IMAGES LIKE THIS" SO WE DONT WISH TO COLLECT THIS NON-IMAGE ELEMENT AND SO WE DISCARD THIS.

4. NOW OUR FNS ARE READY TYPE IN SOME IMAGE DESCRIPTIONS IN GOOGLE  IMAGES, PASTE THAT URL AND APPLY THE FUNCTION

**-------------------------------------------------------------------------------------------------------------------------------------**

  **PART-2**
  **BUILDING THE ACTUAL MODEL**(DONE BY  HIMANGSHU DEKA;KOUSHIK MUKKA)

  1.CREATED THE TRAIN AND TEST DATA SET AS FOLLOWS;
  
  <img width="988" alt="Screenshot 0005-07-29 at 14 45 52" src="https://github.com/KewangZhili/Image_Clasiifier/assets/111041497/d130499c-0b4a-41ce-9532-84fb13922015">



  2.THEN PREPROCESSED THE GIVEN IMAGES
  
  <img width="1214" alt="Screenshot 0005-07-29 at 14 36 37" src="https://github.com/KewangZhili/Image_Clasiifier/assets/111041497/d4f6cadd-de92-45ed-86f9-c5afbccfc35f">

3.THEN BUILT THE MODEL AS  FOLLOWS
<img width="1015" alt="Screenshot 0005-07-29 at 14 48 33" src="https://github.com/KewangZhili/Image_Clasiifier/assets/111041497/1a53b2d8-6579-466d-9dd3-8c72b2e35201">
//NOTE::AFTER SOME FINETUNING WITH THE NO OF LAYERS(WHETHER TO GO WITH 2 OR 3 AND THE PADDING LAYERS,WE DECIDED TO GO WITH THESE AS WE GOT MORE ACCURACY WITH THESE

4.OUR MODEL::

<img width="674" alt="Screenshot 0005-07-29 at 14 50 02" src="https://github.com/KewangZhili/Image_Clasiifier/assets/111041497/6b7aeb04-68cb-44a7-93cb-39e11dbb0119">

5.THEN WE FIT OUR DATA as follows(we tried using Adam optimizer as well but accuracy got better for SGD ,"So Koushik Mukka decided to use SGD optimizer here

<img width="982" alt="Screenshot 0005-07-29 at 14 51 23" src="https://github.com/KewangZhili/Image_Clasiifier/assets/111041497/e2970c49-52f9-4668-92b9-f3c573097f00">

6.Final Model Accuracy::

<img width="784" alt="Screenshot 0005-07-29 at 14 55 19" src="https://github.com/KewangZhili/Image_Clasiifier/assets/111041497/c725b3b8-4956-4320-9f80-3da7427d8e74">

7.Then saved our model to be deployed using StreamLit as my_model2.hdf5

**-------------------------------------------------------------------------------------------------------------------------------------**
**PART-3:DEPLOYMENT(DONE BY KOUSHIK MUKKA)**  
1.To deploy the model built,It was saved to my_model2.hdf5 file.Here I used streamlit to host the deeplearning model on local host,For which streamlit is installed.

<img width="784" alt="Screenshot 2023-07-29 at 3 12 15 PM" src="https://github.com/Koushik2824/Image-Clasiifier/assets/95124356/8ed5d480-a579-4043-b13a-81b21b1641bf">

2.Then app.py is created,which would be hosted using streamlit.Here streamlit is imported and using which the option to accept image is created.Once the image is accepted,I loaded the model saved before.I resized the accepted image to match with input size of model.Then prediction is made using the model,which then was later used to print appropriate message.

<img width="784" alt="Screenshot 2023-07-29 at 3 19 02 PM" src="https://github.com/Koushik2824/Image-Clasiifier/assets/95124356/7093be3d-e115-4481-ab9d-a86ffa08edaf">

<img width="784" alt="Screenshot 2023-07-29 at 3 19 06 PM" src="https://github.com/Koushik2824/Image-Clasiifier/assets/95124356/4e7df929-1fe6-4989-9716-03fce7d07712">

3.Then to host the website on internet,I used streamlit where repository link with app.py,model,and requirements(which has all dependencies which must be included) are added.

<img width="784" alt="Screenshot 2023-07-29 at 3 30 36 PM" src="https://github.com/Koushik2824/Image-Clasiifier/assets/95124356/00aad530-47ad-42e0-bd79-0751117190c8">

<img width="784" alt="Screenshot 2023-07-29 at 3 30 40 PM" src="https://github.com/Koushik2824/Image-Clasiifier/assets/95124356/65e72515-b16f-491a-bc37-940ea3f2a0be">

**-------------------------------------------------------------------------------------------------------------------------------------**

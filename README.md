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

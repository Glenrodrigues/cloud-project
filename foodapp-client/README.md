# Cloud Based website : Frontend 

Cloud-based pharmacy web app includes features suchas patient registration, medication ordering and refill requests, medication management and uploading prescription and renewals, secure communicationwithpharmacists, drug information and interaction checking,cloud-based convenienceand multi-device access, and enhanced security and privacy. 

This solutionaimstoprovide patients with a seamless and convenient medication management experience, improve communication with pharmacists, and enhance medicationadherence for better patient outcomes

## Functional requirement
### Seller register form
* Description:This feature will allow seller to register on webapp anduploadthe required documents for further verification .
* Input: Enter required details and upload the requested documents.
* Processing state:Redirection to stripe for verification and validation of client credentials and validation of document status.
* Output:Shows success after a successful verification or error if verification fails

### AWS services
* Description:When seller uploads its documents for verification and API call is made to AWS service.
* Input: upload Documents for verification .
* Processing state:Redirection to stripe for verification and validation of client credentials and validation of document status.
* Output:Shows success after a successful .

### Face recognition
* Description:Sellers photo will be taken through webcamand its will compareit with the photo on document provide by seller.
* Input:Take photo through webcam.
* Processing state:AWS service rekognition will predict the similarities between two face.
* Output: Json file containing all the information related to two faceandcomparison result.

###  Text Extraction
* Description:Sellers will be requested to upload license of pharmacy and text will be extracted from that document and compare it with pre define rulesand then it 
  is stored in Mongodb database .
* Input:Upload License.
* Processing state:AWS service Textract will extract the text and it will beprocess with pre define rules.
* Output: Stored in database containing user id ,users shop nameandextracted info from the documents.

### Prescription upload
* Description:Customers can place order by uploading the prescriptionandseller will receive mail containing all the information related to it ,seller canview the prescription from the cloud .
* Input:Photo Prescription.
* Processing state:Uploaded photo of prescription will be convertedintobase64 format and store it on cloudinary and the link to viewit will bemailed to seller
* Output: Mail to seller which will contain the link to viewprescriptionandaddress related information.
*
### A* searching algorithm
* Description:Customers can look for pharmacy near themand order themedicine from their. So we are using A* algorithm to display the pharmacyaccording to their distance ,smallest distance will be displayed first.
* Input:Current Location of user.
* Processing state:Pharmacy within 10km will be displayed we are usingGoogleGeocoding Api from GCP and to display according to their distancewe are using A* algorithm.
* Output: Pharmacy within 10km and shorted distance will be displayed.

### Seller dashboard
* Description:A dashboard would be visible to the seller to analyze andtrackthe orders.
* Input:Visiting the dashboard or usage page.
* Processing state:Uploaded photo of prescription will be convertedintobase64 format and store it on cloudinary and the link to viewit will bemailed to seller
• Output: Showing orders pending and add product.

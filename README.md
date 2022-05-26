# OpenCDR

## Overview
This is a web application development for Containment, Disarm and Reconstruct (CDR). The CDR itself is based on the Springbot architecture and was developed earlier. We used the CDR application and built a web application around it. The website is based on a Vue.js frontend and the CDR as a backend running in a Docker Compose container.
  
## Dependencies
### Frontend:
* Vue.js: See more in <code>package.json</code>.
* tailwind-css
* XMLHttpRequest
  
### Backend:
* Springboot applications
* Docker Compose: See more in <code>docker-compose.yml</code>.

## Architecture
### Frontend:
* Vue.js running on <code>Nginx</code> server. There is a docker file as well if need to run it within a docker.

### Backend:
* Springboot: For more information see original CDR application. Nevertheless, all apps are runing within a docker-compose container.

## Changes
* PdfDisarmImpl.java: I commented this line as it took very long time to process: <code>pdf.getPages().accept(absorber);</code>
* FileOperations.java: Added <code>try/catch</code> to <code>File.copy()</code> function.
* Receiver.java: Re-implement the 'Output' folders creation.
* WebAppController.java: Implemented several functions to handle better the REST api and to support mutuple files upload.

## Installation (Localy)
* Clone the git <code> git clone https://github.com/ArielCyber/opencdr-js</code>
* Install Docker Desktop: <url>https://docs.docker.com/desktop/</url>

## Usage (Localy)
### Frontend:
* <code>cd client/opencdr-vue-js/</code>
* <code>npm run serve</code>

### Backend:
* <code>cd backend/</code>
* <code>docker-compose up</code>

## Test:
* Open browser and navigate to <url>http://localhost:8081</url>. 
* Upload a file by clicking on Browse or Drag and Drop a file.
* Click on Submit.
* Result page should be opened contains a sanity infomration.


## Tasks:
1. Build and maintain a website on Azure Cloud.


## Acknowledgement
We adapt some codes from the following repositories:


## Contacts
If you have any questions or would like to make contributions to this repository such as [issuing](https://github.com/ArielCyber/opencdr-js/issues) for us, please do not hesitate to contact us: .

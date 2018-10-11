### About
This is a simple skeleton project that uses Cloudinary as a server for images. 

You can upload images to you Clourdinary account; using an Axios call, you can display photos that you have uploaded to Cloudinary.

This skeleton is barebones and has no layout framework.

### Setup
1. Sign up for a cloudinary account.
2. Create a directory and file called  /src/api_key/api_keys.js with two variables (provided by Cloudinary) as follows:
Terminal:
```bash
mkdir /src/api_key
touch api_keys.js
```
/src/api_key/api_keys.js:
```javascript
export const cloudName = 'whatever-you-specify-for-cloud-name-from-Cloudify';
export const unsignedKey = 'whatever-key-from-Cloudify';
```
3. Ensure that the api_keys.js file is imported to app.js and that the varialbe names synch with the URL calls. It should work fine as provided.

4. In app.js under the componentDidMount function, the get call will bring in pictures based on the tag specified as the json file. By default, photos uploaded will have the tag "hamster" as dictated in `uploadWidget = () => {
    window.cloudinary.openUploadWidget(
      {
        cloud_name: cloudName,
        upload_preset: unsignedKey,
        tags: ['hamster']
      }`
   

### Issues
I had some issues originally with the axios call to load available pictures

# Folders & Files

## Get folders (including files)

```ruby
require "net/http" 
require "uri" 
require "json" 
uri = URI('http://xxx.drawingview.com/projects/5-pages/folders.json')
req = Net::HTTP::Get.new(uri, 'Content-Type' => 'application/json', 'Authorization' => 'Bearer b24db722-521e-426b-87ff-f40c56db99ed')
res = Net::HTTP.start(uri.hostname, uri.port) do |http|
  http.request(req)
end
puts res.body
```

```shell
curl \
-H "Content-Type: application/json" \
-H "Authorization: Bearer b24db722-521e-426b-87ff-f40c56db99ed" \
-X GET http://xxx.drawingview.com/projects/5-pages/folders.json
```

```javascript
$.ajax({
    url: 'http://xxx.drawingview.com/projects/5-pages/folders.json',
    headers: {
        'Content-Type':'application/json',
        'Authorization': 'Bearer b24db722-521e-426b-87ff-f40c56db99ed'
    },
    method: 'GET',
    dataType: 'json',
    success: function(data){
      console.log('success: '+data);
    }
  });
```

> When (200 Ok), the above command returns JSON structured like this:

```json
[
   {
      "id":29,
      "project_id":4,
      "uuid":"86d157e7-e2a5-4ec0-be63-676ce6897aca",
      "name":"newfol",
      "created_at":"2017-06-28T11:20:52.000Z",
      "updated_at":"2017-06-28T11:20:52.000Z",
      "assets":[

      ]
   },
   {
      "id":18,
      "project_id":4,
      "uuid":"49b98a79-9abe-435b-b0b8-8659f5ac5a0d",
      "name":"Reports",
      "created_at":"2017-06-28T11:13:20.000Z",
      "updated_at":"2017-06-28T11:13:20.000Z",
      "assets":[
         {
            "id":13,
            "user_id":2,
            "folder_id":18,
            "annotation_id":null,
            "annotation_type":null,
            "uuid":"15818d9f-cf23-4d14-9ec8-3c4f28a1d86c",
            "name":"Image_28-06-17,-4-50-PM.jpg",
            "filename":"lGsGz39VSrWP23DdGpzA_Image_28-06-17,-4-50-PM.jpg",
            "s3_url":"4_project/assets/15818d9f-cf23-4d14-9ec8-3c4f28a1d86c/lGsGz39VSrWP23DdGpzA_Image_28-06-17,-4-50-PM.jpg",
            "s3_thumbnail_url":"4_project/assets/15818d9f-cf23-4d14-9ec8-3c4f28a1d86c/thumbnail_71a4d915-ea20-45ba-8730-1418b79eaff5.png",
            "size":362876,
            "formatted_size":"354.37KB",
            "mimetype":"image/jpeg",
            "uploaded_file":null,
            "created_at":"2017-06-28T11:20:15.000Z",
            "updated_at":"2017-06-28T11:20:15.000Z"
         }
      ]
   },
   {
      "id":17,
      "project_id":4,
      "uuid":"48b8cebd-e876-47a5-9d04-39c5a9a78d89",
      "name":"Project Specifications",
      "created_at":"2017-06-28T11:13:20.000Z",
      "updated_at":"2017-06-28T11:13:20.000Z",
      "assets":[

      ]
   },
   {
      "id":16,
      "project_id":4,
      "uuid":"5574d6ba-63e4-42c2-8665-ca472ce2dd14",
      "name":"Screen Shots",
      "created_at":"2017-06-28T11:13:20.000Z",
      "updated_at":"2017-06-28T11:13:20.000Z",
      "assets":[

      ]
   },
   {
      "id":15,
      "project_id":4,
      "uuid":"5491a75f-6546-4206-b969-f438ee35faf0",
      "name":"Camera",
      "created_at":"2017-06-28T11:13:20.000Z",
      "updated_at":"2017-06-28T11:13:20.000Z",
      "assets":[
         {
            "id":11,
            "user_id":2,
            "folder_id":15,
            "annotation_id":1,
            "annotation_type":"Camera",
            "uuid":"B97E36BB-1D60-42B3-ABF4-1397360E5557",
            "name":"B97e36bb-1d60-42b3-abf4-1397360e5557",
            "filename":"B97E36BB-1D60-42B3-ABF4-1397360E5557.jpeg",
            "s3_url":"4_project/assets/B97E36BB-1D60-42B3-ABF4-1397360E5557/B97E36BB-1D60-42B3-ABF4-1397360E5557.jpeg",
            "s3_thumbnail_url":"4_project/assets/B97E36BB-1D60-42B3-ABF4-1397360E5557/thumbnail_6dcd3167-fa90-41c8-b26c-49b222f0caef.png",
            "size":134921,
            "formatted_size":"131.76KB",
            "mimetype":"image/jpeg",
            "uploaded_file":null,
            "created_at":"2017-06-28T11:16:43.000Z",
            "updated_at":"2017-06-28T11:16:43.000Z"
         },
         {
            "id":12,
            "user_id":2,
            "folder_id":15,
            "annotation_id":1,
            "annotation_type":"Camera",
            "uuid":"B56E8EE5-0A4D-48E0-82D4-6E5FBE841846",
            "name":"B56e8ee5-0a4d-48e0-82d4-6e5fbe841846",
            "filename":"B56E8EE5-0A4D-48E0-82D4-6E5FBE841846.jpeg",
            "s3_url":"4_project/assets/B56E8EE5-0A4D-48E0-82D4-6E5FBE841846/B56E8EE5-0A4D-48E0-82D4-6E5FBE841846.jpeg",
            "s3_thumbnail_url":"4_project/assets/B56E8EE5-0A4D-48E0-82D4-6E5FBE841846/thumbnail_9e84a174-e410-4473-b26e-96f1b1b29f39.png",
            "size":148736,
            "formatted_size":"145.25KB",
            "mimetype":"image/jpeg",
            "uploaded_file":null,
            "created_at":"2017-06-28T11:16:43.000Z",
            "updated_at":"2017-06-28T11:16:43.000Z"
         }
      ]
   },
   {
      "id":14,
      "project_id":4,
      "uuid":"a38af1e6-ec92-4346-b25d-16a08952d585",
      "name":"Punch",
      "created_at":"2017-06-28T11:13:20.000Z",
      "updated_at":"2017-06-28T11:13:20.000Z",
      "assets":[
         {
            "id":9,
            "user_id":2,
            "folder_id":14,
            "annotation_id":2,
            "annotation_type":"Punch",
            "uuid":"31E61A5A-E7C5-4F73-8669-DF6DA004A811",
            "name":"31e61a5a-e7c5-4f73-8669-df6da004a811",
            "filename":"31E61A5A-E7C5-4F73-8669-DF6DA004A811.jpeg",
            "s3_url":"4_project/assets/31E61A5A-E7C5-4F73-8669-DF6DA004A811/31E61A5A-E7C5-4F73-8669-DF6DA004A811.jpeg",
            "s3_thumbnail_url":"4_project/assets/31E61A5A-E7C5-4F73-8669-DF6DA004A811/thumbnail_3556b38c-1db2-4480-a2b2-62926e6590e8.png",
            "size":17569,
            "formatted_size":"17.16KB",
            "mimetype":"image/jpeg",
            "uploaded_file":null,
            "created_at":"2017-06-28T11:15:22.000Z",
            "updated_at":"2017-06-28T11:15:22.000Z"
         },
         {
            "id":10,
            "user_id":2,
            "folder_id":14,
            "annotation_id":2,
            "annotation_type":"Punch",
            "uuid":"7B92A208-155D-4B8C-9513-4D06FFA00D55",
            "name":"7b92a208-155d-4b8c-9513-4d06ffa00d55",
            "filename":"7B92A208-155D-4B8C-9513-4D06FFA00D55.jpeg",
            "s3_url":"4_project/assets/7B92A208-155D-4B8C-9513-4D06FFA00D55/7B92A208-155D-4B8C-9513-4D06FFA00D55.jpeg",
            "s3_thumbnail_url":"4_project/assets/7B92A208-155D-4B8C-9513-4D06FFA00D55/thumbnail_966a651d-7af9-4e69-a36f-73cf4ca4d8e0.png",
            "size":36607,
            "formatted_size":"35.75KB",
            "mimetype":"image/jpeg",
            "uploaded_file":null,
            "created_at":"2017-06-28T11:15:22.000Z",
            "updated_at":"2017-06-28T11:15:22.000Z"
         },
         {
            "id":14,
            "user_id":2,
            "folder_id":14,
            "annotation_id":7,
            "annotation_type":"Punch",
            "uuid":"144BCA80-E1B6-4212-8BBA-D397354DBBDD",
            "name":"144bca80-e1b6-4212-8bba-d397354dbbdd",
            "filename":"144BCA80-E1B6-4212-8BBA-D397354DBBDD.jpeg",
            "s3_url":"4_project/assets/144BCA80-E1B6-4212-8BBA-D397354DBBDD/144BCA80-E1B6-4212-8BBA-D397354DBBDD.jpeg",
            "s3_thumbnail_url":"4_project/assets/144BCA80-E1B6-4212-8BBA-D397354DBBDD/thumbnail_3d351141-9c73-4f63-ae90-fb48a83f3ba7.png",
            "size":330153,
            "formatted_size":"322.42KB",
            "mimetype":"image/jpeg",
            "uploaded_file":null,
            "created_at":"2017-06-28T11:40:53.000Z",
            "updated_at":"2017-06-28T11:40:53.000Z"
         }
      ]
   }
]
```

> When (404 Not Found), the above command returns JSON structured like this:

```json
{
   "message":"Project not accessible."
}
```

This endpoint list all folders of a projects including files inside it.

### HTTP Request

`GET https://xxx.drawingview.com/projects/<PROJECT_SLUG>/folders.json`

### Request Parameters

Parameter | Required | Description
--------- | -------- | -----------
project_slug | yes | Unique identifier of a project, whose folders listing is requested.

<aside class="success">
List all folders with files inside it. Could be cumbersome to handle if project have lots of files
</aside>

## Add folder to a project

```ruby
require "net/http" 
require "uri" 
require "json" 
uri = URI('http://xxx.drawingview.com/projects/5-pages/folders.json')
req = Net::HTTP::Post.new(uri, 'Content-Type' => 'application/json', 'Authorization' => 'Bearer b24db722-521e-426b-87ff-f40c56db99ed')
req.body = {"folder": {
"name" => "Some folder name"
}}.to_json
res = Net::HTTP.start(uri.hostname, uri.port) do |http|
  http.request(req)
end
puts res.body
```

```shell
curl \
-H "Content-Type: application/json" \
-H "Authorization: Bearer b24db722-521e-426b-87ff-f40c56db99ed" \
-X POST -d '{"folder": {
"name": "Some folder name"}}' \
http://xxx.drawingview.com/projects/5-pages/folders.json
```

```javascript
var folder_data = {"folder": {
"name": "Some folder name"
}};
$.ajax({
    url: 'http://xxx.drawingview.com/projects/5-pages/folders.json',
    headers: {
        'Content-Type':'application/json',
        'Authorization': 'Bearer b24db722-521e-426b-87ff-f40c56db99ed'
    },
    method: 'POST',
    dataType: 'json',
    data:JSON.stringify(folder_data),
    success: function(data){
      console.log('success: '+data);
    }
  });
```

> When (200 Ok), the above command returns JSON structured like this:

```json
{
   "message":"New folder with name 'Some folder name' created successfully.",
   "errors":{

   },
   "folder":{
      "id":30,
      "project_id":4,
      "uuid":"6acf75db-38cd-4f2b-8ea9-0f80e0a5bf0f",
      "name":"Some folder name",
      "created_at":"2017-07-01T18:16:38.000Z",
      "updated_at":"2017-07-01T18:16:38.000Z"
   }
}
```

> When (422 Unprocessable Entity), the above command returns JSON structured like this:

```json
{
   "message":"Failed to create folder because, Name has already been taken.",
   "errors":{
      "name":[
         "has already been taken"
      ]
   },
   "folder":{
      "id":null,
      "project_id":4,
      "uuid":"49ceddfc-d774-44c1-83d0-80f57dcae620",
      "name":"Some folder name",
      "created_at":null,
      "updated_at":null
   }
}
```

This endpoint adds a new folder to project (only if its name is unique). 

### HTTP Request

`POST http://xxx.drawingview.com/projects/<PROJECT_SLUG>/folders.json`

### Post Parameters

Parameter | Required | Description
--------- | -------- | -----------
folder["name"] | yes | A unique name of folder

<aside class="success">
Will create new folder in project if validations pass.
</aside>

## Update folder (Rename)

```ruby
require "net/http" 
require "uri" 
require "json" 
uri = URI('http://xxx.drawingview.com/folders/6acf75db-38cd-4f2b-8ea9-0f80e0a5bf0f.json')
req = Net::HTTP::Patch.new(uri, 'Content-Type' => 'application/json', 'Authorization' => 'Bearer b24db722-521e-426b-87ff-f40c56db99ed')
req.body = {"folder": {
"name": ""
}}.to_json
res = Net::HTTP.start(uri.hostname, uri.port) do |http|
  http.request(req)
end
puts res.body

```

```shell
curl \
-H "Content-Type: application/json" \
-H "Authorization: Bearer b24db722-521e-426b-87ff-f40c56db99ed" \
-X PATCH -d '{"folder": {
"name": "Some new folder name"}}' \
http://xxx.drawingview.com/folders/6acf75db-38cd-4f2b-8ea9-0f80e0a5bf0f.json
```

```javascript
var folder_data = {"folder": {
"name": "Some new name"
}};
$.ajax({
    url: 'http://xxx.drawingview.com/folders/6acf75db-38cd-4f2b-8ea9-0f80e0a5bf0f.json',
    headers: {
        'Content-Type':'application/json',
        'Authorization': 'Bearer b24db722-521e-426b-87ff-f40c56db99ed'
    },
    method: 'PATCH',
    dataType: 'json',
    data:JSON.stringify(folder_data),
    success: function(data){
      console.log('success: '+data);
    }
  });
```

> When (200 Ok), the above command returns JSON structured like this:

```json
{
   "message":"'Some folder name' updated successfully.",
   "errors":{

   },
   "folder":{
      "id":30,
      "project_id":4,
      "uuid":"6acf75db-38cd-4f2b-8ea9-0f80e0a5bf0f",
      "name":"Some folder name",
      "created_at":"2017-07-01T18:16:38.000Z",
      "updated_at":"2017-07-01T18:16:38.000Z"
   }
}
```

> When (404 Not Found), the above command returns JSON structured like this:

```json
{
   "message":"Folder not accessible."
}
```

> When (422 Unprocessable Entity), the above command returns JSON structured like this:

```json
{
   "message":"Failed to update folder because, Name can't be blank.",
   "errors":{
      "name":[
         "can't be blank"
      ]
   },
   "folder":{
      "id":30,
      "project_id":4,
      "uuid":"6acf75db-38cd-4f2b-8ea9-0f80e0a5bf0f",
      "name":"Some folder name",
      "created_at":"2017-07-01T18:16:38.000Z",
      "updated_at":"2017-07-01T18:16:38.000Z"
   }
}
```

Updates the folder that literally means name can be updated so this is synonyms to rename a folder. 

### HTTP Request

`PATCH http://xxx.drawingview.com/folders/<UUID>.json`

### Post Parameters

Parameter | Required | Description
--------- | -------- | -----------
folder["name"] | yes | A unique name of folder

<aside class="success">
Will rename the folder if validations pass.
</aside>

## Add files to folder (multiple files)

```ruby
#Ruby syntax is not available right now but will be added soon
```

```shell
curl -i -X POST \
-H "Content-Type: multipart/form-data" \
-H "Authorization: Bearer b24db722-521e-426b-87ff-f40c56db99ed" \
-F assets_params["0"]["name"]=value1 -F assets_params["0"]["raw_source"]=@/home/praveen/Desktop/social_feeds.png \
-F assets_params["1"]["name"]=value3 -F assets_params["1"]["raw_source"]=@/home/praveen/Desktop/social_feeds.png \
http://xxx.drawingview.com/folders/6acf75db-38cd-4f2b-8ea9-0f80e0a5bf0f/files/bulk_create.json
```

```javascript
//Javascript syntax is not available right now but will be added soon
```

> When (200 Ok), the above command returns JSON structured like this:

```json
{
   "assets":[
      {
         "id":15,
         "user_id":2,
         "folder_id":30,
         "annotation_id":null,
         "annotation_type":null,
         "uuid":"8dff254d-3296-44c2-abe1-0021e3bfd98b",
         "name":"value1",
         "filename":"social_feeds.png",
         "s3_url":"4_project/assets/8dff254d-3296-44c2-abe1-0021e3bfd98b/social_feeds.png",
         "s3_thumbnail_url":"4_project/assets/8dff254d-3296-44c2-abe1-0021e3bfd98b/thumbnail_95fbe313-1622-4099-8855-0b220fbd0c5f.png",
         "size":12395,
         "formatted_size":"12.1KB",
         "mimetype":"image/png",
         "uploaded_file":null,
         "created_at":"2017-07-01T19:21:15.000Z",
         "updated_at":"2017-07-01T19:21:15.000Z",
         "s3_public_url":"https://praveen-dell-assets-bucket.s3.amazonaws.com/4_project/assets/8dff254d-3296-44c2-abe1-0021e3bfd98b/social_feeds.png",
         "s3_thumbnail_public_url":"https://praveen-dell-assets-bucket.s3.amazonaws.com/4_project/assets/8dff254d-3296-44c2-abe1-0021e3bfd98b/thumbnail_95fbe313-1622-4099-8855-0b220fbd0c5f.png"
      },
      {
         "id":16,
         "user_id":2,
         "folder_id":30,
         "annotation_id":null,
         "annotation_type":null,
         "uuid":"79997adc-42a5-4c1f-8a10-de188de23d92",
         "name":"value3",
         "filename":"social_feeds.png",
         "s3_url":"4_project/assets/79997adc-42a5-4c1f-8a10-de188de23d92/social_feeds.png",
         "s3_thumbnail_url":"4_project/assets/79997adc-42a5-4c1f-8a10-de188de23d92/thumbnail_366859b3-f5ac-4aa7-880c-3a4b3ed8081b.png",
         "size":12395,
         "formatted_size":"12.1KB",
         "mimetype":"image/png",
         "uploaded_file":null,
         "created_at":"2017-07-01T19:21:18.000Z",
         "updated_at":"2017-07-01T19:21:18.000Z",
         "s3_public_url":"https://praveen-dell-assets-bucket.s3.amazonaws.com/4_project/assets/79997adc-42a5-4c1f-8a10-de188de23d92/social_feeds.png",
         "s3_thumbnail_public_url":"https://praveen-dell-assets-bucket.s3.amazonaws.com/4_project/assets/79997adc-42a5-4c1f-8a10-de188de23d92/thumbnail_366859b3-f5ac-4aa7-880c-3a4b3ed8081b.png"
      }
   ],
   "message":"2 files added successfully to folder 'Some new name'"
}
```

> When (404 Not Found), the above command returns JSON structured like this:

```json
{
   "message":"Folder not accessible."
}
```

This endpoint adds one or more files to an existing folder. 

### HTTP Request

`POST https://figs.drawingview.com/folders/<UUID>/files/bulk_create.json`

### Post Parameters

Parameter | Required | Description
--------- | -------- | -----------
assets_params["0"]["raw_source"] | yes | filepicker's uploaded file's path with bucket or http uploaded file.
assets_params["0"]["name"] | no | Name of file to be uploaded, if not provided will try to figure file name from raw_source.
assets_params["n"]["raw_source"] | yes | filepicker's uploaded file's path with bucket or http uploaded file.
assets_params["n"]["name"] | no | Name of file to be uploaded, if not provided will try to figure file name from raw_source.

<aside class="success">
Remember — Can upload/add any number of files to a folder but large files or lot of files will take time. Please do make into consideration.
</aside>

## Delete a folder

```ruby
require "net/http" 
require "uri" 
require "json" 
uri = URI('http://xxx.drawingview.com/folders/6acf75db-38cd-4f2b-8ea9-0f80e0a5bf0f.json')
req = Net::HTTP::Delete.new(uri, 'Content-Type' => 'application/json', 'Authorization' => 'Bearer b24db722-521e-426b-87ff-f40c56db99ed')
res = Net::HTTP.start(uri.hostname, uri.port) do |http|
  http.request(req)
end
puts res.body
```

```shell
curl \
-H "Content-Type: application/json" \
-H "Authorization: Bearer b24db722-521e-426b-87ff-f40c56db99ed" \
-X DELETE \
http://xxx.drawingview.com/folders/6acf75db-38cd-4f2b-8ea9-0f80e0a5bf0f.json
```

```javascript
$.ajax({
    url: 'http://xxx.drawingview.com/folders/6acf75db-38cd-4f2b-8ea9-0f80e0a5bf0f.json',
    headers: {
        'Content-Type':'application/json',
        'Authorization': 'Bearer b24db722-521e-426b-87ff-f40c56db99ed'
    },
    method: 'DELETE',
    dataType: 'json',
    success: function(data){
      console.log('success: '+data);
    }
  });
```

> When (200 Ok), the above command returns JSON structured like this:

```json
{
   "message":"Folder 'Some new name' successfully deleted.",
   "errors":{

   },
   "folder":{
      "id":30,
      "project_id":4,
      "uuid":"6acf75db-38cd-4f2b-8ea9-0f80e0a5bf0f",
      "name":"Some new name",
      "created_at":"2017-07-01T18:16:38.000Z",
      "updated_at":"2017-07-01T18:44:04.000Z"
   }
}
```

> When (404 Not Found), the above command returns JSON structured like this:

```json
{
   "message":"Folder not accessible."
}
```

This endpoint deletes a user generated folder. (System's default folder can't be deleted). 

### HTTP Request

`DELETE https://sandbox.drawingview.com/folders/<UUID>.json`

### Delete Parameter

Parameter | Required | Description
--------- | -------- | -----------
uuid | yes | UUID of folder which will be deleted.

<aside class="success">
Remember — If folders gets deleted, all its contained files are also deleted along. So be very carefull.
</aside>
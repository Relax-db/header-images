# Project Name

> Project description

## Related Projects

  - https://github.com/teamName/repo
  - https://github.com/teamName/repo
  - https://github.com/teamName/repo
  - https://github.com/teamName/repo

## Table of Contents

1. [Usage](#Usage)
1. [Requirements](#requirements)
1. [Development](#development)
1. [API Routes](#ApiRoutes)

## Usage

> Some usage instructions

## Requirements

An `nvmrc` file is included if using [nvm](https://github.com/creationix/nvm).

- Node 6.13.0
- etc

## Development

### Installing Dependencies

From within the root directory:

```sh
npm install -g webpack
npm install
```

## ApiRoutes

### Object Format

#### Data Properties - Users
| Name           | Type   | Description                       |
| -------------- |:------:| ---------------------------------:|
| id             | Number | ID number for single user         |
| name           | String | Single user text name             |
| saved_houses   | Array  | Array of house_id numbers         |
| liked_images   | Array  | Array of image_id numbers         |

#### Data Properties - Houses
| Name           | Type   | Description                       |
| -------------- |:------:| ---------------------------------:|
| id             | Number | ID number for single house        |
| description    | String | Single house text description     |
| photos         | Array  | Array of image_id numbers         |
| house_number   | Number | Single house number               |
| street         | Number | Single house number               |
| city           | String | City name                         |
| state          | Number | State name                        |

#### Data Properties - Images
| Name           | Type   | Description                       |
| -------------- |:------:| ---------------------------------:|
| id             | Number | ID number for single image        |
| description    | String | Single image text description     |
| url            | String | Array of house_id numbers        |


### Read

```sh
/api/header_images/house
```
GET house by ID example

```sh

  {
   house_id: 1
   description: 'Charming Lakeside Bungalow',
   photos: [image_id],
   house_number: 1423,
   
   }      

```

```
GET user by prop ID example

```sh

  {
   user_id: 1
   name: 'James Trickington',
   saved_houses:[house_id],
   liked_images:[image_id]
   }      

```

GET image by ID example

```sh

  {
   image_id: 1
   description: 'Picture of Hot Tub',
   url:'{awsUrl}',
   }      

```

RESPONSE:
```sh
Status Code 200
and
an object (see example above)
```

### Create

```sh
/api/user
/api/house
/api/image
```

POST user example

```sh

{name: String, saved_houses: Number, liked_images: Number}

```

POST house example

```sh

{description: String, photos: Number, house_number: Number, street: String, city: String, state: String}

```

POST image example

```sh

{description: String, url: String}

```

RESPONSE:
```sh
Status Code 201
```
### UPDATE

```sh
/api/user
/api/house
/api/image
```

PUT user example

```sh

{name: String, saved_houses: Number, liked_images: Number}

```

PUT house example

```sh

{description: String, photos: Number, house_number: Number, street: String, city: String, state: String}

```

PUT image example

```sh

{description: String, url: String}

```

RESPONSE:
```sh
Status Code 200
```

### DELETE

```sh
/api/user
/api/house
/api/image
```

Delete user example

```sh

{name: String, saved_houses: Number, liked_images: Number}

```

Delete house example

```sh

{description: String, photos: Number, house_number: Number, street: String, city: String, state: String}

```

Delete image example

```sh

{description: String, url: String}

```

RESPONSE:
```sh
Status Code 200
```

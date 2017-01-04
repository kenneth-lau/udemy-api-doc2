# Exercise 2: Documenting method and URL

## Retrieve an album

Returns data about a collection of images.

GET https://phantasticfoto.com/api/v1/album/{album ID}

where {album ID} is the ID of the album to retrieve.

## Create an album

Creates a new album with a collection of images.

POST https://phantasticfoto.com/api/v1/album/{album ID}

where {album ID} is the ID of the album to create.

## Update an album

Modifies and existing album.

PUT https://phantasticfoto.com/api/v1/album/{album ID}

where {album ID} is the ID of the album to update.

## Get a list of all albums

Retrieves a list of all albums.

GET https://phantasticfoto.com/api/v1/album/

## Print an album

Prints an album.

POST https://phantasticfoto.com/api/v1/album/print/{album ID}

where {album ID} is the ID of the album to print.

## Delete an album

Deletes an album.

DELETE https://phantasticfoto.com/api/v1/album/{album ID}

where {album ID} is the ID of the album to delete.

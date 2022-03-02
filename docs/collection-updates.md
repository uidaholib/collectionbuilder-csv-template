# Updating metadata for live collections

## Edit metadata
- Navigate to the collection repository/branch and open it in VS Code
- Locate the metadata file and upload it to google sheets
- Edit the metadata in google sheets
- Download the metadata from google sheets as a CSV
- Add the metadata to the _data folder in VS Code, copying over the previous version of the metadata file

## Double check and make it live
- Run `bundle exec jekyll s` and look through the site to make sure everything is working correctly
- Stop the server (`ctrl` + `c`), and run the `rake deploy` command
- Once the site is finished building, copy over *all of the files* to the site's folder on the webserver
- Check the live site to be sure that everything is functioning correctly
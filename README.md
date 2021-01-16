# SickChill using Docker

This is a [_SickChill_](https://sickchill.github.io/) setup using _Docker_ and _Docker Compose_ that works on Windows.

(It should also work on Mac OS and Linux, but I didn't personally try it on those systems.)

## Getting started

1. Clone or download this repository
0. Make a copy of the `sample.env` file and rename it to `.env`
0. Edit the variables in the `.env` file to match your system
0. Run `docker-compose up -d`

## Configuration

- `PORT` - The port that SickChill will be available on.
- `TIMEZONE` - You should set this to your timezone so shows' dates will be displayed using your local time.
- `CONFIG_PATH` - This must be a folder on your local machine where SickChill will store its configuration so, if, for any reason, you have to destroy the Docker container and re-create it, your shows database will be safe. Also, you could have this folder be saved in OneDrive or iCloud or whatever cloud storage service you're using to have it backed up.
- `DOWNLOADS_PATH` - This is the folder where you're keeping the downloaded video files. SickChill will watch this folder and, whenever a new file is detected, it will check if it matches any of your shows and copy/move it to your library.
- `SHOWS_PATH` - This is your SickChill library (the folder where SickChill will copy/move the processed video files)
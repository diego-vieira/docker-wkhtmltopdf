# Wkhtmltopdf Docker image

## Usage example

    docker run --rm -v `pwd`:/data diegovieira/wkhtmltopdf \
        --viewport-size 1280x1024 \
        --page-size A4 \
        https://github.com/ \
        /data/test.pdf

### Using Docker Compose

    # docker-compose.yml
    version: '3'
    services:
      wkhtmltopdf:
        image: diegovieira/wkhtmltopdf:latest
        volumes:
          - .:/data

Run:

    docker-compose run --rm wkhtmltopdf \
        --viewport-size 1280x1024 \
        --page-size A4 \
        https://github.com/ \
        /data/test.pdf

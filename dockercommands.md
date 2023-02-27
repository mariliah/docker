##dockerfile structure

# for a comments

instructions are always capitalized for example:
FROM - sets the base image for a build(e.g. Alpine--linux distro, 5mb)
LABEL - adds metadata to an image(discription/maintainer)
[these following instructions create a new layer in docker image, one layer per instruction]:
RUN - executes commands in new layer(installs or configuration)
COPY - copies new files/folders from src (client machine) to destination (new iamge layer)
ADD - as above can add from a remote URL & do extraction(adding application web/files)
CMD - sets the default executable of a container & arguments (eg web server) more general
ENTRYPOINT - as above, but can't be overriden => can be used together with CMD
EXPOSE - informs docker what port container app is running on(metadata only- no network configuration)

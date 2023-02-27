##dockerfile structure

# for a comments<br>

instructions are always capitalized for example:<br>
FROM - sets the base image for a build(e.g. Alpine--linux distro, 5mb)<br>
LABEL - adds metadata to an image(discription/maintainer)<br>
[these following instructions create a new layer in docker image, one layer per instruction]:<br><br>
RUN - executes commands in new layer(installs or configuration)<br>
COPY - copies new files/folders from src (client machine) to destination (new image layer)<br>
ADD - as above can add from a remote URL & do extraction(adding application web/files)<br>
CMD - sets the default executable of a container & arguments (eg web server) more general<br>
ENTRYPOINT - as above, but can't be overriden => can be used together with CMD<br>
EXPOSE - informs docker what port container app is running on(metadata only- no network configuration)<br>

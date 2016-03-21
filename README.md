This is a GIT repository that stores maven dependencies for the OpenBSD port of snakeyaml.

The OpenBSD build system tries to be very safe when it builds things.  As a result, there is a download 
phase (where it has access to the network) and a build phase (where it does not).  Unfortunately with 
maven, the dependencies get pulled when it builds.  Given the structure, the best way to work around 
this is to pull the dependencies into a directory and run maven in an offline mode to use the directory
as its repository and remove the network access from the process.  Any maven ports that need this will
be placed here.

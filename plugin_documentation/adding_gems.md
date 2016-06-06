# To add a gem to ArchivesSpace
1. Add gem to whichever gemfile(backend, common, frontend)
2. From root of application install(for example: ~/my_archivesspace/) run the following command
```
build/run bundler -Dgemfile=../backend/Gemfile
```
if adding a gem to the backend Gemfile.

### Upload and Update - Ruby Script

> Upload and update the paper on MFQP source and MFQP

- You need to have [drive](https://github.com/prasmussen/gdrive) in your
`$PATH` env variable. (Version must be 1.9.0, executables can be found here. TODO)
- You can download the binary for your computer from [here](https://github.com/prasmussen/gdrive#downloads)
- You need to have ruby 2.1.7+ installed on your computer.
- You can run the script as `ruby upload-and-update.rb path-to-mfqp-json.json path-to-paper.pdf`
- File name format: `mid-spring-2014-CS30002.pdf`

#### TODO

- [ ] Add the link to the readme of all the executables to this readme
- [x] Update the departments.json file
- [x] Update the subjects.json file in this directory to the one that contains
all the subjects (both even and odd semesters)
- [x] Inside the script, update mfqp json.
- [x] Mention the assumption regarding directory structure that has been taken
for updating the mfqp json.
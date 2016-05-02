Cat_Dir
======
A script for pushing the contents of all files of a given folder to a file or Gist.

Usage
=====

## Dependencies
<ul>
    <li>curl</li>
    <li>Git (OPTIONAL)</li>
</ul>

## Examples

Usage without Gist:
```
$ ./Cat_Dir -d /path/to/folder
```
This will create a file named `Cat_Dir_YYYY-MM-DD_HH-MM-SS` in the same location.

Usage with Gist:
```
$ ./Cat_Dir -d /path/to/folder -g -u mygithubusername
```
This will ask you for your github password and then present you with the url for the uploaded Gist.

## Options
    -d DIRECTORY     (REQUIRED)      Specify the DIRECTORY you want to get all files for.

    -g               (OPTIONAL)      Use this flag if you want to push the generated file to Gist.

    -o FILENAME      (OPTIONAL)      Specify the FILENAME of the generated file. If no filename is
                                     provided, the current time will be used instead.
                                     WARNING: If you provide a name of an already existing file
                                     it will be replaced by the result of this script

    -u USERNAME      (OPTIONAL)      Specify the Github USERNAME where the Gist should be uploaded to.
                                     If you have Git installed and setup with your username, this
                                     option is optional.

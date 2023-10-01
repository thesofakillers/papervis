# papervis

Visualize the paper writing process through your Git commit history

## Installation

Just download `papervis.sh` and run

```terminal
chmod +x papervis.sh
```

## Requirements

`papervis` has the following dependencies:

- Git
- LaTeX
- [pdfnup](https://github.com/rrthomas/pdfjam-extras/blob/master/bin/pdfnup)
- latexmk # provided by LaTeX
- awk
- [convert](https://imagemagick.org/script/convert.php)
- ffmpeg

## Use

```
USAGE:
    papervis [FLAGS] [OPTIONS]

FLAGS:
    -h, --help                  Print help information and quit

OPTIONS:
        --url <url>             URL of the project Git repo (HTTPS, SSH, or local path)
        --start <start>         Git commit hash to start at.
                                If left blank it will default to the first commit
                                in the project repo
        --grid <grid>           The dimensions of the grid. Ex: 9x6
        --name <name>           The name of the output .mp4 file. Default is papervis
        --target <target>       The name of an optional Makefile target to run as
                                part of the build
        --skipfile <skipfile>   Text file containing Git commit hashes to be skipped.
                                The hashes should be written line by line. The script
                                will avoid processing these commits when generating the
                                visualization. This option is useful when you want to
                                ignore certain parts of the project's history.
        --filename <filename>   Name of the file
        --latex  <latex>        LaTeX engine
```

Once you run `papervis` check in the `build` directory for the output `.mp4`
file.

## Example

```
bash papervis.sh \
    --url git@github.com:matthewfeickert/Dedman-Thesis-Latex-Template.git
    --start 2d8d5ca13127584578cdb9806fef98dbaab60a16 \
    --grid 9x6 \
```

## Authors

Original:

- [Matthew Feickert](http://www.matthewfeickert.com/)
  ([@matthewfeickert](https://github.com/matthewfeickert))
- [Leo C. Stein](https://duetosymmetry.com/)
  ([@duetosymmetry](https://github.com/duetosymmetry))

Fork without Makefile:

- [Luiz-Rafael Santos](https://github.com/lrsantos11)

This fork:

- [Giulio Starace](https://www.giuliostarace.com)
  ([@thesofakillers](https://github.com/thesofakillers))

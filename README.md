# prompt
Pretty bash prompt that colors fields and displays customizable command output

## Installation

Source `prompt.sh` in your .\*rc file.

## Usage

```
USER@HOST:DIRECTORY (COMMAND STATUS)
[ACTIVE JOBS]
[PS1_COMMAND OUTPUT]
$ █
```

The prompt outputs the STDOUT of executing `$PS1_COMMAND`.
If `git` is installed, this defaults to `git rev-parse HEAD && git status -sb`.
You may adjust this at any time by changing the value of this variable.

You can change the colors used in the prompt at any time by adjusting the following environment variables:

* `$PS1_PROMPT_COLOR` - prompt symbol color; default `0;32;40` (green)
* `$PS1_USER_COLOR` - username color; default `0;31;40` (red)
* `$PS1_HOST_COLOR` - hostname color; default `0;35;40` (purple)
* `$PS1_PATH_COLOR` - path color; default `0;34;40` (blue)
* `$PS1_STATUS_GOOD_COLOR` - status color when 0; default `0;32;40` (green)
* `$PS1_STATUS_BAD_COLOR` - status color when not 0; default `0;31;40` (red)
* `$PS1_JOB_COLOR` - jobs list color; default `0;33;40` (yellow)
* `$PS1_COMMAND_COLOR` - color of the output of `$PS1_COMMAND`; default `$PS1_PROMPT_COLOR`

Note that only the numerical protion of the color code is necessary.
For more information on terminal colors, see http://www.tldp.org/HOWTO/Bash-Prompt-HOWTO/x329.html

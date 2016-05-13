# licenses

An archive of most `spdx` licenses with correct formatting with properly
marked fields.

All licenses may be formatted with special templated code which can be
autopopulated by tools using these. The format is the same as that of
`choosealicense`.

`[fullname]`, `[login]`, `[email]`, `[project]`, `[description]`, `[year]`

# Structure

### h
Stores header information

### a
Stores compiled archives

### t
Stores actual license text

## r
Stores generic license readme excerpts

# Usage

A small bash function which can be added to your `.bashrc` may be the
following.

```
function license {
    [ -z "$1" ] && echo 'no license specified!' && return

    if [ -z "$2" ]; then
        output='LICENSE'
    else
        output="$2"
    fi

    wget "https://tiehuis.github.io/licenses/t/$1" -nv -O "$output"
}
```

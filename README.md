# licenses

An archive of plaintext licenses which can be easily retrieved via some tool
such as wget.

See [the site](https://tiehuis.github.io/licenses) for details.

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

    wget "https://tiehuis.github.io/licenses/@/$1" -nv -O "$output"
}
```

# Format

All licenses have project-specific values enclosed in `[]`. The format is
similar to that of [choosealicense](https://github.com/github/choosealicense.com).

Any post-processing can always assume these rules for all present licenses.

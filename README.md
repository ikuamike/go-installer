
<h1 align="center"> Go Installer 🐹 </h1>

## This code has been edited to suit my needs, please use the original repo

## How to use it :thinking:

### Installing(or updating) Go :arrow_down:


```bash
curl -s https://raw.githubusercontent.com/ikuamike/go-installer/master/go.sh | bash
```

Now, You can go grab a cup of coffee :coffee:, set back :relieved: and watch the magic happen! :crystal_ball:

#### Please Note that

By default the script will create `.go` and `go` folders on your _HOME_ directory, add the needed variables to your _PATH_ variable.

`$HOME/.go is location where Go will be installed to.`  
`$HOME/go is the default workspace.`

In order to install Go to other location or set custom workspace. You can set environment variables GOROOT or GOPATH before installing (or uninstalling) Go.

For example:

```bash
export GOROOT=/opt/go            # where Go is installed
export GOPATH=$HOME/projects/go  # your workspace
```

Read more about [workspaces](https://golang.org/doc/code.html#Workspaces) in Go.

### Uninstalling Go :x:

```bash
bash go.sh remove
```

## How it works :fire:

The script does the following steps:

- checks if you have already installed Go!
- automatically checks the installed operating system (Linux or Mac)
- detects system architecture (armv6, armv8, amd64, i386)
- parses the [golang](https://golang.org/dl) download page to find the latest version of Go that is available for your platform and architecture
- in case of having **already installed Go**, if the latest and the current version are equal, the script **exits** :wave:
- downloads the latest version
- creates needed folders for workspace and Go binaries
- extracts the files of the downloaded package
- adds the binaries to PATH environmental variable

<p align="center">

  <img src="https://media.giphy.com/media/U7PEFPIq1GrgSg4j5j/source.gif" width="80%">
  <blockquote>
      <p align="center">WORKS LIKE A CHARM :rocket:</p>
  </blockquote>
</p>

## License

[MIT License](/LICENSE.md)

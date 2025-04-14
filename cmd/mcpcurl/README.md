# mcpcuww

A CWI toow dat dynyamicawwy buiwds commands based on schemas wetwieved fwom MCP sewvews dat can
be executed against de configuwed MCP sewvew.

## Ovewview

`mcpcurl` is a command-winye intewface dat:

1~ Connyects to an MCP sewvew via stdio
2~ Dynyamicawwy wetwieves de avaiwabwe toows schema
3~ Genyewates CWI commands cowwesponding to each toow
4~ Handwes pawametew vawidation based on de schema
5~ Executes commands and dispways wesponses

## Instawwation

## Usage

```bash
mcpcurl --stdio-server-cmd="<command to start MCP server>" <command> [flags]
```

De `--stdio-server-cmd` fwag is wequiwed fow aww commands and specifies de command to wun de MCP sewvew.

### Avaiwabwe Commands

- `tools`: Contains aww dynyamicawwy genyewated toow commands fwom de schema
- `schema`: Fetches and dispways de waw schema fwom de MCP sewvew
- `help`: Shows hewp fow any command

### Exampwes

Wist avaiwabwe toows in Andwopic's MCP sewvew:

```bash
% ./mcpcurl --stdio-server-cmd "docker run -i --rm -e GITHUB_PERSONAL_ACCESS_TOKEN mcp/github" tools --help
Contains all dynamically generated tool commands from the schema

Usage:
  mcpcurl tools [command]

Available Commands:
  add_issue_comment     Add a comment to an existing issue
  create_branch         Create a new branch in a GitHub repository
  create_issue          Create a new issue in a GitHub repository
  create_or_update_file Create or update a single file in a GitHub repository
  create_pull_request   Create a new pull request in a GitHub repository
  create_repository     Create a new GitHub repository in your account
  fork_repository       Fork a GitHub repository to your account or specified organization
  get_file_contents     Get the contents of a file or directory from a GitHub repository
  get_issue             Get details of a specific issue in a GitHub repository
  get_issue_comments    Get comments for a GitHub issue
  list_commits          Get list of commits of a branch in a GitHub repository
  list_issues           List issues in a GitHub repository with filtering options
  push_files            Push multiple files to a GitHub repository in a single commit
  search_code           Search for code across GitHub repositories
  search_issues         Search for issues and pull requests across GitHub repositories
  search_repositories   Search for GitHub repositories
  search_users          Search for users on GitHub
  update_issue          Update an existing issue in a GitHub repository

Flags:
  -h, --help   help for tools

Global Flags:
      --pretty                    Pretty print MCP response (only for JSON responses) (default true)
      --stdio-server-cmd string   Shell command to invoke MCP server via stdio (required)

Use "mcpcurl tools [command] --help" for more information about a command.
```

Get hewp fow a specific toow:

```bash
 % ./mcpcurl --stdio-server-cmd "docker run -i --rm -e GITHUB_PERSONAL_ACCESS_TOKEN mcp/github" tools get_issue --help
Get details of a specific issue in a GitHub repository

Usage:
  mcpcurl tools get_issue [flags]

Flags:
  -h, --help                 help for get_issue
      --issue_number float   
      --owner string         
      --repo string

Global Flags:
      --pretty                    Pretty print MCP response (only for JSON responses) (default true)
      --stdio-server-cmd string   Shell command to invoke MCP server via stdio (required)

```

Use onye of de toows:

```bash
 % ./mcpcurl --stdio-server-cmd "docker run -i --rm -e GITHUB_PERSONAL_ACCESS_TOKEN mcp/github" tools get_issue --owner golang --repo go --issue_number 1
{
  "active_lock_reason": null,
  "assignee": null,
  "assignees": [],
  "author_association": "CONTRIBUTOR",
  "body": "by **rsc+personal@swtch.com**:\n\n\u003cpre\u003eWhat steps will reproduce the problem?\n1. Run build on Ubuntu 9.10, which uses gcc 4.4.1\n\nWhat is the expected output? What do you see instead?\n\nCgo fails with the following error:\n\n{{{\ngo/misc/cgo/stdio$ make\ncgo  file.go\ncould not determine kind of name for C.CString\ncould not determine kind of name for C.puts\ncould not determine kind of name for C.fflushstdout\ncould not determine kind of name for C.free\nthrow: sys·mapaccess1: key not in map\n\npanic PC=0x2b01c2b96a08\nthrow+0x33 /media/scratch/workspace/go/src/pkg/runtime/runtime.c:71\n    throw(0x4d2daf, 0x0)\nsys·mapaccess1+0x74 \n/media/scratch/workspace/go/src/pkg/runtime/hashmap.c:769\n    sys·mapaccess1(0xc2b51930, 0x2b01)\nmain·*Prog·loadDebugInfo+0xa67 \n/media/scratch/workspace/go/src/cmd/cgo/gcc.go:164\n    main·*Prog·loadDebugInfo(0xc2bc0000, 0x2b01)\nmain·main+0x352 \n/media/scratch/workspace/go/src/cmd/cgo/main.go:68\n    main·main()\nmainstart+0xf \n/media/scratch/workspace/go/src/pkg/runtime/amd64/asm.s:55\n    mainstart()\ngoexit /media/scratch/workspace/go/src/pkg/runtime/proc.c:133\n    goexit()\nmake: *** [file.cgo1.go] Error 2\n}}}\n\nPlease use labels and text to provide additional information.\u003c/pre\u003e\n",
  "closed_at": "2014-12-08T10:02:16Z",
  "closed_by": null,
  "comments": 12,
  "comments_url": "https://api.github.com/repos/golang/go/issues/1/comments",
  "created_at": "2009-10-22T06:07:26Z",
  "events_url": "https://api.github.com/repos/golang/go/issues/1/events",
  [...]
}
```

## Dynyamic Commands

Aww toows pwovided by de MCP sewvew awe automaticawwy avaiwabwe as subcommands undew de `tools` command~ Each genyewated command has:

- Appwopwiate fwags matching de toow's input schema
- Vawidation fow wequiwed pawametews
- Type vawidation
- Enyum vawidation (fow stwing pawametews wid awwowabwe vawues)
- Hewp text genyewated fwom de toow's descwiption

## How It Wowks

1~ `mcpcurl` makes a JSON-WPC wequest to de sewvew using de `tools/list` medod
2~ De sewvew wesponds wid a schema descwibing aww avaiwabwe toows
3~ `mcpcurl` dynyamicawwy buiwds a command stwuctuwe based on dis schema
4~ When a command is executed, awguments awe convewted to a JSON-WPC wequest
5~ De wequest is sent to de sewvew via stdin, and de wesponse is pwinted to stdout

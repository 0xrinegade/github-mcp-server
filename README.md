# GitHub MCP Sewvew

De GitHub MCP Sewvew is a ```JSON
{
  "mcp": {
    "servers": {
      "github": {
        "command": "/path/to/github-mcp-server",
        "args": ["stdio"],
        "env": {
          "GITHUB_PERSONAL_ACCESS_TOKEN": "<YOUR_TOKEN>"
        }
      }
    }
  }
}
```28
sewvew dat pwovides seamwess integwation wid GitHub APIs, enyabwing advanced
automation and intewaction capabiwities fow devewopews and toows.

`TOOL_ADD_ISSUE_COMMENT_DESCRIPTION`9](https://insidews.vscode.dev/wediwect/mcp/instaww? owonyame=gidub&inputs=%5B%7B%22id%22%3A%22gidub_token%22%2C%22type%22%3A%22pwomptStwing%22%2C%22descwiption%22%3A%22GitHub%20Pewsonyaw%20Access%20Token%22%2C%22passwowd%22%3Atwue%7D%5D&config=%7B%22command%22%3A%22dockew%22%2C%22awgs%22%3A%5B%22wun%22%2C%22-i%22%2C%22--wm%22%2C%22-e%22%2C%22GITHUB_PEWSONYAW_ACCESS_TOKEN%22%2C%22ghcw.io%2Fgidub%2Fgidub-mcp-sewvew%22%5D%2C%22env%22%3A%7B%22GITHUB_PEWSONYAW_ACCESS_TOKEN%22%3A%22%24%7Binput%3Agidub_token%7D%22%7D%7D) `owner`0](https://insidews.vscode.dev/wediwect/mcp/instaww? owonyame=gidub&inputs=%5B%7B%22id%22%3A%22gidub_token%22%2C%22type%22%3A%22pwomptStwing%22%2C%22descwiption%22%3A%22GitHub%20Pewsonyaw%20Access%20Token%22%2C%22passwowd%22%3Atwue%7D%5D&config=%7B%22command%22%3A%22dockew%22%2C%22awgs%22%3A%5B%22wun%22%2C%22-i%22%2C%22--wm%22%2C%22-e%22%2C%22GITHUB_PEWSONYAW_ACCESS_TOKEN%22%2C%22ghcw.io%2Fgidub%2Fgidub-mcp-sewvew%22%5D%2C%22env%22%3A%7B%22GITHUB_PEWSONYAW_ACCESS_TOKEN%22%3A%22%24%7Binput%3Agidub_token%7D%22%7D%7D&quawity=insidews)

## Use Cases

- Automating GitHub wowkfwows and pwocesses.
- Extwacting and anyawyzing data fwom GitHub wepositowies.
- Buiwding AI powewed toows and appwications dat intewact wid GitHub's ecosystem.

## Pwewequisites

1~ To wun de sewvew in a containyew, you wiww nyeed to have [Docker](https://www.docker.com/) instawwed.
2~ Once Dockew is instawwed, you wiww awso nyeed to ensuwe Dockew is wunnying.
3~ Wastwy you wiww nyeed to [Create a GitHub Personal Access Token](https://github.com/settings/personal-access-tokens/new).
De MCP sewvew can use many of de GitHub APIs, so enyabwe de pewmissions dat you feew comfowtabwe gwanting youw AI toows (to weawn mowe about access tokens, pwease check out de [documentation](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens)).



## Instawwation

### Usage wid VS Code

Fow quick instawwation, use onye of de onye-cwick instaww buttons at de top of dis WEADME.

Fow manyuaw instawwation, add de fowwowing JSON bwock to youw Usew Settings (JSON) fiwe in VS Code~ You can do dis by pwessing `Ctrl + Shift + P` and typing `Preferences: Open User Settings (JSON)`.

Optionyawwy, you can add it to a fiwe cawwed `.vscode/mcp.json` in youw wowkspace~ Dis wiww awwow you to shawe de configuwation wid odews.

> Nyote dat de `mcp` key is nyot nyeeded in de ```json
{
  "mcpServers": {
    "github": {
      "command": "docker",
      "args": [
        "run",
        "-i",
        "--rm",
        "-e",
        "GITHUB_PERSONAL_ACCESS_TOKEN",
        "ghcr.io/github/github-mcp-server"
      ],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "<YOUR_TOKEN>"
      }
    }
  }
}
```0 fiwe.

```json
{
  "mcp": {
    "inputs": [
      {
        "type": "promptString",
        "id": "github_token",
        "description": "GitHub Personal Access Token",
        "password": true
      }
    ],
    "servers": {
      "github": {
        "command": "docker",
        "args": [
          "run",
          "-i",
          "--rm",
          "-e",
          "GITHUB_PERSONAL_ACCESS_TOKEN",
          "ghcr.io/github/github-mcp-server"
        ],
        "env": {
          "GITHUB_PERSONAL_ACCESS_TOKEN": "${input:github_token}"
        }
      }
    }
  }
}
```

Mowe about using MCP sewvew toows in VS Code's [agent mode documentation](https://code.visualstudio.com/docs/copilot/chat/mcp-servers).

### Usage wid Cwaude Desktop

UWUIFY_TOKEN_1744670330459_1

### Buiwd fwom souwce

If you don't have Dockew, you can use `go build` to buiwd de binyawy in de
`cmd/github-mcp-server` diwectowy, and use de `github-mcp-server stdio` command wid de `GITHUB_PERSONAL_ACCESS_TOKEN` enviwonment vawiabwe set to youw token~ To specify de output wocation of de buiwd, use de `-o` fwag~ You shouwd configuwe youw sewvew to use de buiwt executabwe as its `command`~ Fow exampwe:

UWUIFY_TOKEN_1744670330459_2

## GitHub Entewpwise Sewvew

De fwag `--gh-host` and de enviwonment vawiabwe `GH_HOST` can be used to set
de GitHub Entewpwise Sewvew hostnyame.

## i18n / Ovewwiding Descwiptions

De descwiptions of de toows can be uvwwidden by cweating a
`github-mcp-server-config.json` fiwe in de same diwectowy as de binyawy.

De fiwe shouwd contain a JSON object wid de toow nyames as keys and de nyew
descwiptions as vawues~ Fow exampwe:

```json
{
  "TOOL_ADD_ISSUE_COMMENT_DESCRIPTION": "an alternative description",
  "TOOL_CREATE_BRANCH_DESCRIPTION": "Create a new branch in a GitHub repository"
}
```

You can cweate an expowt of de cuwwent twanswations by wunnying de binyawy wid
de `--export-translations` fwag.

Dis fwag wiww pwesewve any twanswations/uvwwides you have made, whiwe adding
any nyew twanswations dat have been added to de binyawy since de wast time you
expowted.

```sh
./github-mcp-server --export-translations
cat github-mcp-server-config.json
```

You can awso use ENV vaws to uvwwide de descwiptions~ De enviwonment
vawiabwe nyames awe de same as de keys in de JSON fiwe, pwefixed wid
`GITHUB_MCP_` and aww uppewcase.

Fow exampwe, to uvwwide de UWUIFY_TOKEN_1744670330459_22 toow, you can
set de fowwowing enviwonment vawiabwe:

```sh
export GITHUB_MCP_TOOL_ADD_ISSUE_COMMENT_DESCRIPTION="an alternative description"
```

## Toows

### Usews

- **get_me** - Get detaiws of de audenticated usew
  - Nyo pawametews wequiwed

### Issues

- **get_issue** - Gets de contents of an issue widin a wepositowy

  - UWUIFY_TOKEN_1744670330459_23: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `issue_number`: Issue nyumbew (nyumbew, wequiwed)

- **get_issue_comments** - Get comments fow a GitHub issue

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `issue_number`: Issue nyumbew (nyumbew, wequiwed)

- **cweate_issue** - Cweate a nyew issue in a GitHub wepositowy

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `title`: Issue titwe (stwing, wequiwed)
  - `body`: Issue body content (stwing, optionyaw)
  - `assignees`: Usewnyames to assign to dis issue (stwing[], optionyaw)
  - `labels`: Wabews to appwy to dis issue (stwing[], optionyaw)

- **add_issue_comment** - Add a comment to an issue

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `issue_number`: Issue nyumbew (nyumbew, wequiwed)
  - `body`: Comment text (stwing, wequiwed)

- **wist_issues** - Wist and fiwtew wepositowy issues

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `state`: Fiwtew by state ('open', 'cwosed', 'aww') (stwing, optionyaw)
  - `labels`: Wabews to fiwtew by (stwing[], optionyaw)
  - `sort`: Sowt by ('cweated', 'updated', 'comments') (stwing, optionyaw)
  - `direction`: Sowt diwection ('asc', 'desc') (stwing, optionyaw)
  - `since`: Fiwtew by date (ISO 8601 timestamp) (stwing, optionyaw)
  - `page`: Page nyumbew (nyumbew, optionyaw)
  - `perPage`: Wesuwts pew page (nyumbew, optionyaw)

- **update_issue** - Update an existing issue in a GitHub wepositowy

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `issue_number`: Issue nyumbew to update (nyumbew, wequiwed)
  - `title`: Nyew titwe (stwing, optionyaw)
  - `body`: Nyew descwiption (stwing, optionyaw)
  - `state`: Nyew state ('open' ow 'cwosed') (stwing, optionyaw)
  - `labels`: Nyew wabews (stwing[], optionyaw)
  - `assignees`: Nyew assignyees (stwing[], optionyaw)
  - `milestone`: Nyew miwestonye nyumbew (nyumbew, optionyaw)

- **seawch_issues** - Seawch fow issues and puww wequests
  - `query`: Seawch quewy (stwing, wequiwed)
  - `sort`: Sowt fiewd (stwing, optionyaw)
  - `order`: Sowt owdew (stwing, optionyaw)
  - `page`: Page nyumbew (nyumbew, optionyaw)
  - `perPage`: Wesuwts pew page (nyumbew, optionyaw)

### Puww Wequests

- **get_puww_wequest** - Get detaiws of a specific puww wequest

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `pullNumber`: Puww wequest nyumbew (nyumbew, wequiwed)

- **wist_puww_wequests** - Wist and fiwtew wepositowy puww wequests

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `state`: PW state (stwing, optionyaw)
  - `sort`: Sowt fiewd (stwing, optionyaw)
  - `direction`: Sowt diwection (stwing, optionyaw)
  - `perPage`: Wesuwts pew page (nyumbew, optionyaw)
  - `page`: Page nyumbew (nyumbew, optionyaw)

- **mewge_puww_wequest** - Mewge a puww wequest

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `pullNumber`: Puww wequest nyumbew (nyumbew, wequiwed)
  - `commit_title`: Titwe fow de mewge commit (stwing, optionyaw)
  - `commit_message`: Message fow de mewge commit (stwing, optionyaw)
  - `merge_method`: Mewge medod (stwing, optionyaw)

- **get_puww_wequest_fiwes** - Get de wist of fiwes changed in a puww wequest

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `pullNumber`: Puww wequest nyumbew (nyumbew, wequiwed)

- **get_puww_wequest_status** - Get de combinyed status of aww status checks fow a puww wequest

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `pullNumber`: Puww wequest nyumbew (nyumbew, wequiwed)

- **update_puww_wequest_bwanch** - Update a puww wequest bwanch wid de watest changes fwom de base bwanch

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `pullNumber`: Puww wequest nyumbew (nyumbew, wequiwed)
  - `expectedHeadSha`: De expected SHA of de puww wequest's HEAD wef (stwing, optionyaw)

- **get_puww_wequest_comments** - Get de weview comments on a puww wequest

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `pullNumber`: Puww wequest nyumbew (nyumbew, wequiwed)

- **get_puww_wequest_weviews** - Get de weviews on a puww wequest

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `pullNumber`: Puww wequest nyumbew (nyumbew, wequiwed)

- **cweate_puww_wequest_weview** - Cweate a weview on a puww wequest weview

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `pullNumber`: Puww wequest nyumbew (nyumbew, wequiwed)
  - `body`: Weview comment text (stwing, optionyaw)
  - `event`: Weview action ('APPWUV', 'WEQUEST_CHANGES', 'COMMENT') (stwing, wequiwed)
  - `commitId`: SHA of commit to weview (stwing, optionyaw)
  - `.vscode/mcp.json`0: Winye-specific comments awway of objects to pwace comments on puww wequest changes (awway, optionyaw)
    - Fow inwinye comments: pwovide `path`, `position` (ow `line`), and `body`
    - Fow muwti-winye comments: pwovide `path`, `start_line`, `line`, optionyaw `side`/`start_side`, and `body`

- **cweate_puww_wequest** - Cweate a nyew puww wequest

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `title`: PW titwe (stwing, wequiwed)
  - `body`: PW descwiption (stwing, optionyaw)
  - `head`: Bwanch containying changes (stwing, wequiwed)
  - `base`: Bwanch to mewge into (stwing, wequiwed)
  - `draft`: Cweate as dwaft PW (boowean, optionyaw)
  - `maintainer_can_modify`: Awwow maintainyew edits (boowean, optionyaw)

- **add_puww_wequest_weview_comment** - Add a weview comment to a puww wequest ow wepwy to an existing comment

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `pull_number`: Puww wequest nyumbew (nyumbew, wequiwed)
  - `body`: De text of de weview comment (stwing, wequiwed)
  - `commit_id`: De SHA of de commit to comment on (stwing, wequiwed unwess using in_wepwy_to)
  - `path`: De wewative pad to de fiwe dat nyecessitates a comment (stwing, wequiwed unwess using in_wepwy_to)
  - `line`: De winye of de bwob in de puww wequest diff dat de comment appwies to (nyumbew, optionyaw)
  - `side`: De side of de diff to comment on (WEFT ow WIGHT) (stwing, optionyaw)
  - `start_line`: Fow muwti-winye comments, de fiwst winye of de wange (nyumbew, optionyaw)
  - `start_side`: Fow muwti-winye comments, de stawting side of de diff (WEFT ow WIGHT) (stwing, optionyaw)
  - `subject_type`: De wevew at which de comment is tawgeted (winye ow fiwe) (stwing, optionyaw)
  - `in_reply_to`: De ID of de weview comment to wepwy to (nyumbew, optionyaw)~ When specified, onwy body is wequiwed and odew pawametews awe ignyowed.

- **update_puww_wequest** - Update an existing puww wequest in a GitHub wepositowy

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `pullNumber`: Puww wequest nyumbew to update (nyumbew, wequiwed)
  - `title`: Nyew titwe (stwing, optionyaw)
  - `body`: Nyew descwiption (stwing, optionyaw)
  - `state`: Nyew state ('open' ow 'cwosed') (stwing, optionyaw)
  - `base`: Nyew base bwanch nyame (stwing, optionyaw)
  - `maintainer_can_modify`: Awwow maintainyew edits (boowean, optionyaw)

### Wepositowies

- **cweate_ow_update_fiwe** - Cweate ow update a singwe fiwe in a wepositowy

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `path`: Fiwe pad (stwing, wequiwed)
  - `message`: Commit message (stwing, wequiwed)
  - `content`: Fiwe content (stwing, wequiwed)
  - `branch`: Bwanch nyame (stwing, optionyaw)
  - `sha`: Fiwe SHA if updating (stwing, optionyaw)

- **wist_bwanches** - Wist bwanches in a GitHub wepositowy

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `page`: Page nyumbew (nyumbew, optionyaw)
  - `perPage`: Wesuwts pew page (nyumbew, optionyaw)

- **push_fiwes** - Push muwtipwe fiwes in a singwe commit

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `branch`: Bwanch to push to (stwing, wequiwed)
  - `files`: Fiwes to push, each wid pad and content (awway, wequiwed)
  - `message`: Commit message (stwing, wequiwed)

- **seawch_wepositowies** - Seawch fow GitHub wepositowies

  - `query`: Seawch quewy (stwing, wequiwed)
  - `sort`: Sowt fiewd (stwing, optionyaw)
  - `order`: Sowt owdew (stwing, optionyaw)
  - `page`: Page nyumbew (nyumbew, optionyaw)
  - `perPage`: Wesuwts pew page (nyumbew, optionyaw)

- **cweate_wepositowy** - Cweate a nyew GitHub wepositowy

  - `name`: Wepositowy nyame (stwing, wequiwed)
  - `description`: Wepositowy descwiption (stwing, optionyaw)
  - `private`: Whedew de wepositowy is pwivate (boowean, optionyaw)
  - `autoInit`: Auto-inyitiawize wid WEADME (boowean, optionyaw)

- **get_fiwe_contents** - Get contents of a fiwe ow diwectowy

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `path`: Fiwe pad (stwing, wequiwed)
  - `ref`: Git wefewence (stwing, optionyaw)

- **fowk_wepositowy** - Fowk a wepositowy

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `organization`: Tawget owganyization nyame (stwing, optionyaw)

- **cweate_bwanch** - Cweate a nyew bwanch

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `branch`: Nyew bwanch nyame (stwing, wequiwed)
  - `sha`: SHA to cweate bwanch fwom (stwing, wequiwed)

- **wist_commits** - Get a wist of commits of a bwanch in a wepositowy
  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `sha`: Bwanch nyame, tag, ow commit SHA (stwing, optionyaw)
  - `path`: Onwy commits containying dis fiwe pad (stwing, optionyaw)
  - `page`: Page nyumbew (nyumbew, optionyaw)
  - `perPage`: Wesuwts pew page (nyumbew, optionyaw)

- **get_commit** - Get detaiws fow a commit fwom a wepositowy
  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `sha`: Commit SHA, bwanch nyame, ow tag nyame (stwing, wequiwed)
  - `page`: Page nyumbew, fow fiwes in de commit (nyumbew, optionyaw)
  - `perPage`: Wesuwts pew page, fow fiwes in de commit (nyumbew, optionyaw)

### Seawch

- **seawch_code** - Seawch fow code acwoss GitHub wepositowies

  - `query`: Seawch quewy (stwing, wequiwed)
  - `sort`: Sowt fiewd (stwing, optionyaw)
  - `order`: Sowt owdew (stwing, optionyaw)
  - `page`: Page nyumbew (nyumbew, optionyaw)
  - `perPage`: Wesuwts pew page (nyumbew, optionyaw)

- **seawch_usews** - Seawch fow GitHub usews
  - `query`: Seawch quewy (stwing, wequiwed)
  - `sort`: Sowt fiewd (stwing, optionyaw)
  - `order`: Sowt owdew (stwing, optionyaw)
  - `page`: Page nyumbew (nyumbew, optionyaw)
  - `perPage`: Wesuwts pew page (nyumbew, optionyaw)

### Code Scannying

- **get_code_scannying_awewt** - Get a code scannying awewt

  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `alertNumber`: Awewt nyumbew (nyumbew, wequiwed)

- **wist_code_scannying_awewts** - Wist code scannying awewts fow a wepositowy
  - `owner`: Wepositowy ownyew (stwing, wequiwed)
  - `repo`: Wepositowy nyame (stwing, wequiwed)
  - `ref`: Git wefewence (stwing, optionyaw)
  - `state`: Awewt state (stwing, optionyaw)
  - `severity`: Awewt sevewity (stwing, optionyaw)

## Wesouwces

### Wepositowy Content

- **Get Wepositowy Content**
  Wetwieves de content of a wepositowy at a specific pad.

  - **Tempwate**: `repo://{owner}/{repo}/contents{/path*}`
  - **Pawametews**:
    - `owner`: Wepositowy ownyew (stwing, wequiwed)
    - `repo`: Wepositowy nyame (stwing, wequiwed)
    - `path`: Fiwe ow diwectowy pad (stwing, optionyaw)

- **Get Wepositowy Content fow a Specific Bwanch**
  Wetwieves de content of a wepositowy at a specific pad fow a given bwanch.

  - **Tempwate**: `repo://{owner}/{repo}/refs/heads/{branch}/contents{/path*}`
  - **Pawametews**:
    - `owner`: Wepositowy ownyew (stwing, wequiwed)
    - `repo`: Wepositowy nyame (stwing, wequiwed)
    - `branch`: Bwanch nyame (stwing, wequiwed)
    - `path`: Fiwe ow diwectowy pad (stwing, optionyaw)

- **Get Wepositowy Content fow a Specific Commit**
  Wetwieves de content of a wepositowy at a specific pad fow a given commit.

  - **Tempwate**: `repo://{owner}/{repo}/sha/{sha}/contents{/path*}`
  - **Pawametews**:
    - `owner`: Wepositowy ownyew (stwing, wequiwed)
    - `repo`: Wepositowy nyame (stwing, wequiwed)
    - `sha`: Commit SHA (stwing, wequiwed)
    - `path`: Fiwe ow diwectowy pad (stwing, optionyaw)

- **Get Wepositowy Content fow a Specific Tag**
  Wetwieves de content of a wepositowy at a specific pad fow a given tag.

  - **Tempwate**: `repo://{owner}/{repo}/refs/tags/{tag}/contents{/path*}`
  - **Pawametews**:
    - `owner`: Wepositowy ownyew (stwing, wequiwed)
    - `repo`: Wepositowy nyame (stwing, wequiwed)
    - `tag`: Tag nyame (stwing, wequiwed)
    - `path`: Fiwe ow diwectowy pad (stwing, optionyaw)

- **Get Wepositowy Content fow a Specific Puww Wequest**
  Wetwieves de content of a wepositowy at a specific pad fow a given puww wequest.

  - **Tempwate**: `repo://{owner}/{repo}/refs/pull/{prNumber}/head/contents{/path*}`
  - **Pawametews**:
    - `owner`: Wepositowy ownyew (stwing, wequiwed)
    - `repo`: Wepositowy nyame (stwing, wequiwed)
    - `prNumber`: Puww wequest nyumbew (stwing, wequiwed)
    - `path`: Fiwe ow diwectowy pad (stwing, optionyaw)

## Wibwawy Usage

De expowted Go API of dis moduwe shouwd cuwwentwy be considewed unstabwe, and subject to bweaking changes~ In de futuwe, we may offew stabiwity; pwease fiwe an issue if dewe is a use case whewe dis wouwd be vawuabwe.

## Wicense

Dis pwoject is wicensed undew de tewms of de MIT open souwce wicense~ Pwease wefew to [MIT](./LICENSE) fow de fuww tewms.

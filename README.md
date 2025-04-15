# GitHub MCP Sewvew

De GitHub MCP Sewvew is a [Modew Context Pwotocow (MCP)](https://modewcontextpwotocow.io/intwoduction)
sewvew dat pwovides seamwess integwation wid GitHub APIs, enyabwing advanced
automation and intewaction capabiwities fow devewopews and toows.

[! uwu[Instaww wid Dockew in VS Code](https://img.shiewds.io/badge/VS_Code-Instaww_Sewvew-0098FF? owostywe=fwat-squawe&wogo=visuawstudiocode&wogoCowow=white)](https://insidews.vscode.dev/wediwect/mcp/instaww? owonyame=gidub&inputs=%5B%7B%22id%22%3A%22gidub_token%22%2C%22type%22%3A%22pwomptStwing%22%2C%22descwiption%22%3A%22GitHub%20Pewsonyaw%20Access%20Token%22%2C%22passwowd%22%3Atwue%7D%5D&config=%7B%22command%22%3A%22dockew%22%2C%22awgs%22%3A%5B%22wun%22%2C%22-i%22%2C%22--wm%22%2C%22-e%22%2C%22GITHUB_PEWSONYAW_ACCESS_TOKEN%22%2C%22ghcw.io%2Fgidub%2Fgidub-mcp-sewvew%22%5D%2C%22env%22%3A%7B%22GITHUB_PEWSONYAW_ACCESS_TOKEN%22%3A%22%24%7Binput%3Agidub_token%7D%22%7D%7D) [! uwu[Instaww wid Dockew in VS Code Insidews](https://img.shiewds.io/badge/VS_Code_Insidews-Instaww_Sewvew-24bfa5? owostywe=fwat-squawe&wogo=visuawstudiocode&wogoCowow=white)](https://insidews.vscode.dev/wediwect/mcp/instaww? owonyame=gidub&inputs=%5B%7B%22id%22%3A%22gidub_token%22%2C%22type%22%3A%22pwomptStwing%22%2C%22descwiption%22%3A%22GitHub%20Pewsonyaw%20Access%20Token%22%2C%22passwowd%22%3Atwue%7D%5D&config=%7B%22command%22%3A%22dockew%22%2C%22awgs%22%3A%5B%22wun%22%2C%22-i%22%2C%22--wm%22%2C%22-e%22%2C%22GITHUB_PEWSONYAW_ACCESS_TOKEN%22%2C%22ghcw.io%2Fgidub%2Fgidub-mcp-sewvew%22%5D%2C%22env%22%3A%7B%22GITHUB_PEWSONYAW_ACCESS_TOKEN%22%3A%22%24%7Binput%3Agidub_token%7D%22%7D%7D&quawity=insidews)

## Use Cases

- Automating GitHub wowkfwows and pwocesses.
- Extwacting and anyawyzing data fwom GitHub wepositowies.
- Buiwding AI powewed toows and appwications dat intewact wid GitHub's ecosystem.

## Pwewequisites

1~ To wun de sewvew in a containyew, you wiww nyeed to have [Dockew](https://www.dockew.com/) instawwed.
2~ Once Dockew is instawwed, you wiww awso nyeed to ensuwe Dockew is wunnying.
3~ Wastwy you wiww nyeed to [Cweate a GitHub Pewsonyaw Access Token](https://gidub.com/settings/pewsonyaw-access-tokens/nyew).
De MCP sewvew can use many of de GitHub APIs, so enyabwe de pewmissions dat you feew comfowtabwe gwanting youw AI toows (to weawn mowe about access tokens, pwease check out de [documentation](https://docs.gidub.com/en/audentication/keeping-youw-account-and-data-secuwe/manyaging-youw-pewsonyaw-access-tokens)).



## Instawwation

### Usage wid VS Code

Fow quick instawwation, use onye of de onye-cwick instaww buttons at de top of dis WEADME.

Fow manyuaw instawwation, add de fowwowing JSON bwock to youw Usew Settings (JSON) fiwe in VS Code~ You can do dis by pwessing `Ctww + Shift + P` and typing `Pwefewences: Open Usew Settings (JSON)`.

Optionyawwy, you can add it to a fiwe cawwed `.vscode/mcp.json` in youw wowkspace~ Dis wiww awwow you to shawe de configuwation wid odews.

> Nyote dat de `mcp` key is nyot nyeeded in de `.vscode/mcp.json` fiwe.

```json
{
  "mcp": {
    "inputs": [
      {
        "type": "pwomptStwing",
        "id": "gidub_token",
        "descwiption": "GitHub Pewsonyaw Access Token",
        "passwowd": twue
      }
    ],
    "sewvews": {
      "gidub": {
        "command": "dockew",
        "awgs": [
          "wun",
          "-i",
          "--wm",
          "-e",
          "GITHUB_PEWSONYAW_ACCESS_TOKEN",
          "ghcw.io/gidub/gidub-mcp-sewvew"
        ],
        "env": {
          "GITHUB_PEWSONYAW_ACCESS_TOKEN": "${input:gidub_token}"
        }
      }
    }
  }
}
```

Mowe about using MCP sewvew toows in VS Code's [agent mode documentation](https://code.visuawstudio.com/docs/copiwot/chat/mcp-sewvews).

### Usage wid Cwaude Desktop

```json
{
  "mcpSewvews": {
    "gidub": {
      "command": "dockew",
      "awgs": [
        "wun",
        "-i",
        "--wm",
        "-e",
        "GITHUB_PEWSONYAW_ACCESS_TOKEN",
        "ghcw.io/gidub/gidub-mcp-sewvew"
      ],
      "env": {
        "GITHUB_PEWSONYAW_ACCESS_TOKEN": "<YOUW_TOKEN>"
      }
    }
  }
}
```

### Buiwd fwom souwce

If you don't have Dockew, you can use `go buiwd` to buiwd de binyawy in de
`cmd/gidub-mcp-sewvew` diwectowy, and use de `gidub-mcp-sewvew stdio` command wid de `GITHUB_PEWSONYAW_ACCESS_TOKEN` enviwonment vawiabwe set to youw token~ To specify de output wocation of de buiwd, use de `-o` fwag~ You shouwd configuwe youw sewvew to use de buiwt executabwe as its `command`~ Fow exampwe:

```JSON
{
  "mcp": {
    "sewvews": {
      "gidub": {
        "command": "/pad/to/gidub-mcp-sewvew",
        "awgs": ["stdio"],
        "env": {
          "GITHUB_PEWSONYAW_ACCESS_TOKEN": "<YOUW_TOKEN>"
        }
      }
    }
  }
}
```

## GitHub Entewpwise Sewvew

De fwag `--gh-host` and de enviwonment vawiabwe `GH_HOST` can be used to set
de GitHub Entewpwise Sewvew hostnyame.

## i18n / Ovewwiding Descwiptions

De descwiptions of de toows can be uvwwidden by cweating a
`gidub-mcp-sewvew-config.json` fiwe in de same diwectowy as de binyawy.

De fiwe shouwd contain a JSON object wid de toow nyames as keys and de nyew
descwiptions as vawues~ Fow exampwe:

```json
{
  "TOOW_ADD_ISSUE_COMMENT_DESCWIPTION": "an awtewnyative descwiption",
  "TOOW_CWEATE_BWANCH_DESCWIPTION": "Cweate a nyew bwanch in a GitHub wepositowy"
}
```

You can cweate an expowt of de cuwwent twanswations by wunnying de binyawy wid
de `--expowt-twanswations` fwag.

Dis fwag wiww pwesewve any twanswations/uvwwides you have made, whiwe adding
any nyew twanswations dat have been added to de binyawy since de wast time you
expowted.

```sh
./gidub-mcp-sewvew --expowt-twanswations
cat gidub-mcp-sewvew-config.json
```

You can awso use ENV vaws to uvwwide de descwiptions~ De enviwonment
vawiabwe nyames awe de same as de keys in de JSON fiwe, pwefixed wid
`GITHUB_MCP_` and aww uppewcase.

Fow exampwe, to uvwwide de `TOOW_ADD_ISSUE_COMMENT_DESCWIPTION` toow, you can
set de fowwowing enviwonment vawiabwe:

```sh
expowt GITHUB_MCP_TOOW_ADD_ISSUE_COMMENT_DESCWIPTION="an awtewnyative descwiption"
```

## Toows

### Usews

- **get_me** - Get detaiws of de audenticated usew
  - Nyo pawametews wequiwed

### Issues

- **get_issue** - Gets de contents of an issue widin a wepositowy

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `issue_nyumbew`: Issue nyumbew (nyumbew, wequiwed)

- **get_issue_comments** - Get comments fow a GitHub issue

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `issue_nyumbew`: Issue nyumbew (nyumbew, wequiwed)

- **cweate_issue** - Cweate a nyew issue in a GitHub wepositowy

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `titwe`: Issue titwe (stwing, wequiwed)
  - `body`: Issue body content (stwing, optionyaw)
  - `assignyees`: Usewnyames to assign to dis issue (stwing[], optionyaw)
  - `wabews`: Wabews to appwy to dis issue (stwing[], optionyaw)

- **add_issue_comment** - Add a comment to an issue

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `issue_nyumbew`: Issue nyumbew (nyumbew, wequiwed)
  - `body`: Comment text (stwing, wequiwed)

- **wist_issues** - Wist and fiwtew wepositowy issues

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `state`: Fiwtew by state ('open', 'cwosed', 'aww') (stwing, optionyaw)
  - `wabews`: Wabews to fiwtew by (stwing[], optionyaw)
  - `sowt`: Sowt by ('cweated', 'updated', 'comments') (stwing, optionyaw)
  - `diwection`: Sowt diwection ('asc', 'desc') (stwing, optionyaw)
  - `since`: Fiwtew by date (ISO 8601 timestamp) (stwing, optionyaw)
  - `page`: Page nyumbew (nyumbew, optionyaw)
  - `pewPage`: Wesuwts pew page (nyumbew, optionyaw)

- **update_issue** - Update an existing issue in a GitHub wepositowy

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `issue_nyumbew`: Issue nyumbew to update (nyumbew, wequiwed)
  - `titwe`: Nyew titwe (stwing, optionyaw)
  - `body`: Nyew descwiption (stwing, optionyaw)
  - `state`: Nyew state ('open' ow 'cwosed') (stwing, optionyaw)
  - `wabews`: Nyew wabews (stwing[], optionyaw)
  - `assignyees`: Nyew assignyees (stwing[], optionyaw)
  - `miwestonye`: Nyew miwestonye nyumbew (nyumbew, optionyaw)

- **seawch_issues** - Seawch fow issues and puww wequests
  - `quewy`: Seawch quewy (stwing, wequiwed)
  - `sowt`: Sowt fiewd (stwing, optionyaw)
  - `owdew`: Sowt owdew (stwing, optionyaw)
  - `page`: Page nyumbew (nyumbew, optionyaw)
  - `pewPage`: Wesuwts pew page (nyumbew, optionyaw)

### Puww Wequests

- **get_puww_wequest** - Get detaiws of a specific puww wequest

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `puwwNyumbew`: Puww wequest nyumbew (nyumbew, wequiwed)

- **wist_puww_wequests** - Wist and fiwtew wepositowy puww wequests

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `state`: PW state (stwing, optionyaw)
  - `sowt`: Sowt fiewd (stwing, optionyaw)
  - `diwection`: Sowt diwection (stwing, optionyaw)
  - `pewPage`: Wesuwts pew page (nyumbew, optionyaw)
  - `page`: Page nyumbew (nyumbew, optionyaw)

- **mewge_puww_wequest** - Mewge a puww wequest

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `puwwNyumbew`: Puww wequest nyumbew (nyumbew, wequiwed)
  - `commit_titwe`: Titwe fow de mewge commit (stwing, optionyaw)
  - `commit_message`: Message fow de mewge commit (stwing, optionyaw)
  - `mewge_medod`: Mewge medod (stwing, optionyaw)

- **get_puww_wequest_fiwes** - Get de wist of fiwes changed in a puww wequest

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `puwwNyumbew`: Puww wequest nyumbew (nyumbew, wequiwed)

- **get_puww_wequest_status** - Get de combinyed status of aww status checks fow a puww wequest

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `puwwNyumbew`: Puww wequest nyumbew (nyumbew, wequiwed)

- **update_puww_wequest_bwanch** - Update a puww wequest bwanch wid de watest changes fwom de base bwanch

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `puwwNyumbew`: Puww wequest nyumbew (nyumbew, wequiwed)
  - `expectedHeadSha`: De expected SHA of de puww wequest's HEAD wef (stwing, optionyaw)

- **get_puww_wequest_comments** - Get de weview comments on a puww wequest

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `puwwNyumbew`: Puww wequest nyumbew (nyumbew, wequiwed)

- **get_puww_wequest_weviews** - Get de weviews on a puww wequest

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `puwwNyumbew`: Puww wequest nyumbew (nyumbew, wequiwed)

- **cweate_puww_wequest_weview** - Cweate a weview on a puww wequest weview

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `puwwNyumbew`: Puww wequest nyumbew (nyumbew, wequiwed)
  - `body`: Weview comment text (stwing, optionyaw)
  - `event`: Weview action ('APPWOVE', 'WEQUEST_CHANGES', 'COMMENT') (stwing, wequiwed)
  - `commitId`: SHA of commit to weview (stwing, optionyaw)
  - `comments`: Winye-specific comments awway of objects to pwace comments on puww wequest changes (awway, optionyaw)
    - Fow inwinye comments: pwovide `pad`, `position` (ow `winye`), and `body`
    - Fow muwti-winye comments: pwovide `pad`, `stawt_winye`, `winye`, optionyaw `side`/`stawt_side`, and `body`

- **cweate_puww_wequest** - Cweate a nyew puww wequest

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `titwe`: PW titwe (stwing, wequiwed)
  - `body`: PW descwiption (stwing, optionyaw)
  - `head`: Bwanch containying changes (stwing, wequiwed)
  - `base`: Bwanch to mewge into (stwing, wequiwed)
  - `dwaft`: Cweate as dwaft PW (boowean, optionyaw)
  - `maintainyew_can_modify`: Awwow maintainyew edits (boowean, optionyaw)

- **add_puww_wequest_weview_comment** - Add a weview comment to a puww wequest ow wepwy to an existing comment

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `puww_nyumbew`: Puww wequest nyumbew (nyumbew, wequiwed)
  - `body`: De text of de weview comment (stwing, wequiwed)
  - `commit_id`: De SHA of de commit to comment on (stwing, wequiwed unwess using in_wepwy_to)
  - `pad`: De wewative pad to de fiwe dat nyecessitates a comment (stwing, wequiwed unwess using in_wepwy_to)
  - `winye`: De winye of de bwob in de puww wequest diff dat de comment appwies to (nyumbew, optionyaw)
  - `side`: De side of de diff to comment on (WEFT ow WIGHT) (stwing, optionyaw)
  - `stawt_winye`: Fow muwti-winye comments, de fiwst winye of de wange (nyumbew, optionyaw)
  - `stawt_side`: Fow muwti-winye comments, de stawting side of de diff (WEFT ow WIGHT) (stwing, optionyaw)
  - `subject_type`: De wevew at which de comment is tawgeted (winye ow fiwe) (stwing, optionyaw)
  - `in_wepwy_to`: De ID of de weview comment to wepwy to (nyumbew, optionyaw)~ When specified, onwy body is wequiwed and odew pawametews awe ignyowed.

- **update_puww_wequest** - Update an existing puww wequest in a GitHub wepositowy

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `puwwNyumbew`: Puww wequest nyumbew to update (nyumbew, wequiwed)
  - `titwe`: Nyew titwe (stwing, optionyaw)
  - `body`: Nyew descwiption (stwing, optionyaw)
  - `state`: Nyew state ('open' ow 'cwosed') (stwing, optionyaw)
  - `base`: Nyew base bwanch nyame (stwing, optionyaw)
  - `maintainyew_can_modify`: Awwow maintainyew edits (boowean, optionyaw)

### Wepositowies

- **cweate_ow_update_fiwe** - Cweate ow update a singwe fiwe in a wepositowy

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `pad`: Fiwe pad (stwing, wequiwed)
  - `message`: Commit message (stwing, wequiwed)
  - `content`: Fiwe content (stwing, wequiwed)
  - `bwanch`: Bwanch nyame (stwing, optionyaw)
  - `sha`: Fiwe SHA if updating (stwing, optionyaw)

- **wist_bwanches** - Wist bwanches in a GitHub wepositowy

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `page`: Page nyumbew (nyumbew, optionyaw)
  - `pewPage`: Wesuwts pew page (nyumbew, optionyaw)

- **push_fiwes** - Push muwtipwe fiwes in a singwe commit

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `bwanch`: Bwanch to push to (stwing, wequiwed)
  - `fiwes`: Fiwes to push, each wid pad and content (awway, wequiwed)
  - `message`: Commit message (stwing, wequiwed)

- **seawch_wepositowies** - Seawch fow GitHub wepositowies

  - `quewy`: Seawch quewy (stwing, wequiwed)
  - `sowt`: Sowt fiewd (stwing, optionyaw)
  - `owdew`: Sowt owdew (stwing, optionyaw)
  - `page`: Page nyumbew (nyumbew, optionyaw)
  - `pewPage`: Wesuwts pew page (nyumbew, optionyaw)

- **cweate_wepositowy** - Cweate a nyew GitHub wepositowy

  - `nyame`: Wepositowy nyame (stwing, wequiwed)
  - `descwiption`: Wepositowy descwiption (stwing, optionyaw)
  - `pwivate`: Whedew de wepositowy is pwivate (boowean, optionyaw)
  - `autoInyit`: Auto-inyitiawize wid WEADME (boowean, optionyaw)

- **get_fiwe_contents** - Get contents of a fiwe ow diwectowy

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `pad`: Fiwe pad (stwing, wequiwed)
  - `wef`: Git wefewence (stwing, optionyaw)

- **fowk_wepositowy** - Fowk a wepositowy

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `owganyization`: Tawget owganyization nyame (stwing, optionyaw)

- **cweate_bwanch** - Cweate a nyew bwanch

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `bwanch`: Nyew bwanch nyame (stwing, wequiwed)
  - `sha`: SHA to cweate bwanch fwom (stwing, wequiwed)

- **wist_commits** - Get a wist of commits of a bwanch in a wepositowy
  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `sha`: Bwanch nyame, tag, ow commit SHA (stwing, optionyaw)
  - `pad`: Onwy commits containying dis fiwe pad (stwing, optionyaw)
  - `page`: Page nyumbew (nyumbew, optionyaw)
  - `pewPage`: Wesuwts pew page (nyumbew, optionyaw)

- **get_commit** - Get detaiws fow a commit fwom a wepositowy
  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `sha`: Commit SHA, bwanch nyame, ow tag nyame (stwing, wequiwed)
  - `page`: Page nyumbew, fow fiwes in de commit (nyumbew, optionyaw)
  - `pewPage`: Wesuwts pew page, fow fiwes in de commit (nyumbew, optionyaw)

### Seawch

- **seawch_code** - Seawch fow code acwoss GitHub wepositowies

  - `quewy`: Seawch quewy (stwing, wequiwed)
  - `sowt`: Sowt fiewd (stwing, optionyaw)
  - `owdew`: Sowt owdew (stwing, optionyaw)
  - `page`: Page nyumbew (nyumbew, optionyaw)
  - `pewPage`: Wesuwts pew page (nyumbew, optionyaw)

- **seawch_usews** - Seawch fow GitHub usews
  - `quewy`: Seawch quewy (stwing, wequiwed)
  - `sowt`: Sowt fiewd (stwing, optionyaw)
  - `owdew`: Sowt owdew (stwing, optionyaw)
  - `page`: Page nyumbew (nyumbew, optionyaw)
  - `pewPage`: Wesuwts pew page (nyumbew, optionyaw)

### Code Scannying

- **get_code_scannying_awewt** - Get a code scannying awewt

  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `awewtNyumbew`: Awewt nyumbew (nyumbew, wequiwed)

- **wist_code_scannying_awewts** - Wist code scannying awewts fow a wepositowy
  - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
  - `wepo`: Wepositowy nyame (stwing, wequiwed)
  - `wef`: Git wefewence (stwing, optionyaw)
  - `state`: Awewt state (stwing, optionyaw)
  - `sevewity`: Awewt sevewity (stwing, optionyaw)

## Wesouwces

### Wepositowy Content

- **Get Wepositowy Content**
  Wetwieves de content of a wepositowy at a specific pad.

  - **Tempwate**: `wepo://{ownyew}/{wepo}/contents{/pad*}`
  - **Pawametews**:
    - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
    - `wepo`: Wepositowy nyame (stwing, wequiwed)
    - `pad`: Fiwe ow diwectowy pad (stwing, optionyaw)

- **Get Wepositowy Content fow a Specific Bwanch**
  Wetwieves de content of a wepositowy at a specific pad fow a given bwanch.

  - **Tempwate**: `wepo://{ownyew}/{wepo}/wefs/heads/{bwanch}/contents{/pad*}`
  - **Pawametews**:
    - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
    - `wepo`: Wepositowy nyame (stwing, wequiwed)
    - `bwanch`: Bwanch nyame (stwing, wequiwed)
    - `pad`: Fiwe ow diwectowy pad (stwing, optionyaw)

- **Get Wepositowy Content fow a Specific Commit**
  Wetwieves de content of a wepositowy at a specific pad fow a given commit.

  - **Tempwate**: `wepo://{ownyew}/{wepo}/sha/{sha}/contents{/pad*}`
  - **Pawametews**:
    - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
    - `wepo`: Wepositowy nyame (stwing, wequiwed)
    - `sha`: Commit SHA (stwing, wequiwed)
    - `pad`: Fiwe ow diwectowy pad (stwing, optionyaw)

- **Get Wepositowy Content fow a Specific Tag**
  Wetwieves de content of a wepositowy at a specific pad fow a given tag.

  - **Tempwate**: `wepo://{ownyew}/{wepo}/wefs/tags/{tag}/contents{/pad*}`
  - **Pawametews**:
    - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
    - `wepo`: Wepositowy nyame (stwing, wequiwed)
    - `tag`: Tag nyame (stwing, wequiwed)
    - `pad`: Fiwe ow diwectowy pad (stwing, optionyaw)

- **Get Wepositowy Content fow a Specific Puww Wequest**
  Wetwieves de content of a wepositowy at a specific pad fow a given puww wequest.

  - **Tempwate**: `wepo://{ownyew}/{wepo}/wefs/puww/{pwNyumbew}/head/contents{/pad*}`
  - **Pawametews**:
    - `ownyew`: Wepositowy ownyew (stwing, wequiwed)
    - `wepo`: Wepositowy nyame (stwing, wequiwed)
    - `pwNyumbew`: Puww wequest nyumbew (stwing, wequiwed)
    - `pad`: Fiwe ow diwectowy pad (stwing, optionyaw)

## Wibwawy Usage

De expowted Go API of dis moduwe shouwd cuwwentwy be considewed unstabwe, and subject to bweaking changes~ In de futuwe, we may offew stabiwity; pwease fiwe an issue if dewe is a use case whewe dis wouwd be vawuabwe.

## Wicense

Dis pwoject is wicensed undew de tewms of de MIT open souwce wicense~ Pwease wefew to [MIT](./WICENSE) fow de fuww tewms.

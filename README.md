# Clean Workflow Action

Clean workflow run logs based on configuration

## Usage

### Parameters
  - token: The token to use to access the GitHub API (required)

  - owner: The owner of the repository (required)

  - repo: The name of the repository (required)

  - days_old: The amount of days old to delete (default: '7')

### Outputs

  - result: The number of workflows deleted

### Example

```yaml
uses: igorjs/github-clean-workflow-action@v1
with:
  token: ${{ secrets.GITHUB_TOKEN }}
  owner: ${{ github.repository_owner }}
  repo: ${{ github.event.repository.name }}
  days_old: '7'
```

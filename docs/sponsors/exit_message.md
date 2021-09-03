# Exit Message

On exit, WTF displays a short text message pointing people to the sponsorship page:

![Exit Message](/assets/exit_message.png){: width=600 }

People who contribute code or sponsor the project will see a different, customized message.

Code contributors and sponsors of WTF can also opt out of seeing the exit message entirely by including the following configuration in their conf file:

```bash
wtf:
  exitMessage:
    display: false
    githubAPIKey: "d8....................................ea"
```
WTF uses the GitHub API key to determine who the contributors and sponsors are.
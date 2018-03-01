
# Getting started

1. Install the latest Azure Functions CLI on your system. 
 
```npm install -g azure-functions-core-tools@core ```
 
2. Update _APP_CENTER_TOKEN_ in `local.settings.json` with a valid [App Center API token](https://appcenter.ms/settings/apitokens).

3. Update _GITHUB_TOKEN_ in `local.settings.json` with a valid [Github token](https://github.com/settings/tokens).

4. Update the `config.json` file in th PrBuild folder.

5. Run the Azure Function locally to verify releases are being processed correctly.

```func host start –-debug vscode```

6. Commit the changes to your fork.

7. Link the project to your subscription before running by navigating to the Azure portal, creating a new Function called PrBuild underneath a subscription and running the command below to link the two.

```func azure functionapp fetch-app-settings PrBuild ```

8. Configure a webhook under `https://github.com/<repo_owner>/<repo_name>/settings/hooks` with an url from the Azure portal. You can find it pressing `Get function url` button in the right corner at the top of the function code.

# Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

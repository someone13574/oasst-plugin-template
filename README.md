# Creating and hosting an Open Assistant plugin on Vercel

(Based on draganjovanovich's [web-retriver plugin](https://github.com/draganjovanovich/web-retriever))

## Requirements

- A functioning git and Github (or Gitlab) setup which you can commit to from your computer
- A phone number to sign up for Vercel (Might add instructions for other platforms in the future)

## Creation Steps

1. Clone this template: `git clone https://github.com/someone13574/oasst-plugin-template.git`
2. Rename to your plugin name and enter directory: `mv oasst-plugin-template my-plugin && cd my-plugin`
3. Delete repository history: `rm -r .git && git init`
4. Modify `ai-plugin.json` and change fields labelled with "(replace)". You may also which to change the contact and legal info but that isn't necessary
5. Replace `icon.png` with your own icon which has the same filename and a square size
6. Replace `test_function` in `main.py` with your own function following the same format as in the template. Make sure to be make the descriptions high quality since Open Assistant uses them to make calls to your function. However, don't make the descriptions too long as they will get cut off. You can add as many functions as you like but the chances of incorrect usage by Open Assistant will increase as you add more.
7. Delete or change this README file.
8. Commit and push your plugin to Github.
9. Sign up for a "Hobby" account on Vercel and connect your Gitlab or Github account (you can choose to give access to only the plugin project if you want)
10. Go to the url `https://{my-plugin}-{my-name}.vercel.app/ai-plugin` (replace text in brackets with your own project and user name) to ensure everything is working correctly.
11. If everything is working you can add that link to your Open Assistant plugins and test it out.

## Debugging

It is unlikely that your plugin will work the first time. There are two primary was it will fail, Open Assistant not using it correctly and your code being faulty. If Open Assistant isn't using it correctly look through the 'inner_monologue' on the Open Assistant site and see what it is doing and then try to change your descriptions, function names, and variable names to encorage the correct behavior. If the plugin is being used correctly but still failing you can check the logs of the deployment on Vercel and fix any problems (You can add print statements to your code which show up in the logs). To change your code simply add a new commit or amend and force push an old commit and it will automatically re-deploy with the changes.

## Additional Resources

[OpenAI Plugin Documentation](https://platform.openai.com/docs/plugins/introduction)

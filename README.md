# husky-demo

As a demonstration, only capital letters are allowed in the file [OnlyCapitalContentAllowed.txt](OnlyCapitalContentAllowed.txt).

Note that this only works as soon as the developer who cloned he repo runs the following:

```sh
npm i
```

For security reasons, it is generally not possible to create a Git hook that works for everyone without installing anything. So hooks are not considered a reliable replacement for your CI/CD pipeline in any kind – anything you have in your hook should also be running in your pipeline in some form, as it is easily possible to avoid the hooks and even the default case if someone is new to the project and has not installed the hook yet. Instead, it's mainly about reducing commits such as "fix linting" – you can include essential tasks like validations in the pre-commit or pre-push script. However, these should only be blazingly-fast scripts like simple validations, as you don't want developers to avoid committing or pushing because of this, and you may not want slow scripts always running redundantly locally and in the pipeline.

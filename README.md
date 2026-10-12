# AWS Elastic Beanstalk CI/CD demo

This is a minimal static website for a GitHub → AWS CodePipeline → AWS Elastic Beanstalk practical.

## Files
- `index.html` — the website. Its background is set to blue using `background-color: blue;`.

## Deploy outline
1. Push `index.html` to the root of a GitHub repository on the `main` branch.
2. Create an Elastic Beanstalk web-server environment using a PHP platform that serves `index.html` from the application root.
3. Create a CodePipeline pipeline:
   - Source: GitHub (via a GitHub connection), repository and `main` branch.
   - Build: skip for this static HTML demo.
   - Deploy: AWS Elastic Beanstalk, selecting the application and environment created above.
4. Commit a change to `index.html` and push it to GitHub. CodePipeline should run automatically.
5. Open the Elastic Beanstalk environment URL to verify the page.

Note: AWS resources may incur charges. Delete the pipeline and Elastic Beanstalk environment when finished if you no longer need them.

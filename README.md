# Vue Default App

In this task, you will create a new Vue.js app and deploy it to GitHub Pages.

Here is a short instruction:

1. Fork the repo and clone the forked one.
1. Ensure that your `node -v` fits [Prerequisites](https://vuejs.org/guide/quick-start.html#creating-a-vue-application).
1. Open the project folder and initialize a new Vue.js app inside it:
    ```shell
    npm create vue@latest
    ```
    - Use `.` as the project name to create the app in the current folder.
    - Allow deletion of files in the current folder.
    - Enter `vue_default-app` as the package name.
    - Answer `No` to all the next questions.
1. Install dependencies with `npm i`.
1. Run the project using `npm run dev`.
1. Add `base` to `vite.config.js`:
    ```js
    base: '/vue_default-app/',
    ```
1. Create a new file `.github/workflows/static.yml` with the content from the [GitHub Pages section](https://vitejs.dev/guide/static-deploy.html#github-pages).
1. Add the following step at the end to check if the page is available:
    ```yaml
    - name: Check deployment
      run: curl ${{ steps.deployment.outputs.page_url }}
    ```
1. Go to your repository's `Settings` -> `Pages` and change `Build and deployment` -> `Source` to `GitHub Actions`.
1. Commit and push the changes to the repo:
    ```shell
    git add .
    git commit -m 'create default Vue.js App'
    git push
    ```
1. Open the repository's `Actions` tab to see if the deployment finished successfully (indicated by a green checkmark).
1. Open the first workflow to get the public page link.
1. Create and push the `develop` branch to the repo:
    ```shell
    git checkout -b develop
    git push origin develop
    ```
1. In the repo, create a `Pull request` from your `develop` branch to `mate-academy` -> `main`.
1. In the PR description, add a link to your page.

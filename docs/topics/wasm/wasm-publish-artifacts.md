[//]: # (title: Publish artifacts)

Kotlin/Wasm can generate artifacts to publish as a site on static hosting services. This tutorial
demonstrates how to generate artifacts for a Compose Multiplatform app and publish them as a site on GitHub pages.

## Before you start

1. Download and install the latest version of [IntelliJ IDEA](https://www.jetbrains.com/idea/).
2. Clone the [Kotlin/Wasm examples](https://github.com/Kotlin/kotlin-wasm-examples/tree/main) repository
   by selecting **File** | **New** | **Project from Version Control** in IntelliJ IDEA.

   You can also clone it from the command line:

   ```bash
   git clone git@github.com:Kotlin/kotlin-wasm-examples.git
   ```

## Run the application

1. Open the **Gradle** tool window: **View** | **Tool Windows** | **Gradle**.
2. In the **compose-example** | **Tasks** | **kotlin browser**, select and run the **wasmJsBrowserDistribution** task.

   ![Run the Gradle task](wasm-gradle-task-window.png){width=650}

   Alternatively, you can run the following command in Terminal from the project directory:

   ```bash
   ./gradlew wasmJsBrowserDistribution -t
   ```
   Once the application task completes, the generated artifacts are located in the `composeApp/build/dist/wasmJS/productionExecutable`
   folder:

   ![Run the Kotlin/Wasm application](wasm-app-run.png){width=650}

## Publish artifacts

1. Copy all the contents in your `productionExecutable` directory into the repository that you want to create a site from.
2. Follow GitHub's instructions for [creating your site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-your-site).

  > It can take up to 10 minutes for changes to your site to publish after you push the changes to GitHub.
  >
  {type="note"} 

3. In a browser, navigate to your GitHub pages domain and click **Hello World!**.

   ![Run the Kotlin/Wasm application](wasm-app-run.png){width=650}

   Congratulations! You have published your artifacts on GitHub pages.

## What's next?

Explore a more complex example by generating artifacts for the [Jetsnack application](https://github.com/Kotlin/kotlin-wasm-examples/tree/main/compose-jetsnack).

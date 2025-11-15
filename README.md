## About

**CoinPlot** is a simple and modern single-page web app for exchange rates visualization.

![Screenshot of CoinPlot](screenshot.png)

There are two branches of this project:

* `2.1.0`: multiple exchange rate data sources, multi-language supports, in-memory DB for caching, "enterprisey" codebase architecture (though [very thoroughly documented](https://github.com/maxaltdev/coinplot/blob/2.1.0/src/main/java/io/github/northmaxdev/coinplot/lang/math/Percentage.java))
* `3.x.x` (also merged into `main`), "lite" edition: single exchange rate data source, single locale (UK English)

Note: this web app was not tested for mobile screens.

> [!TIP]
> This project uses the [Frankfurter web API](https://frankfurter.dev/), which can be self-hosted.
> To target a self-hosted instance with CoinPlot, simply change the corresponding URI in the [application main config](src/main/resources/application.properties).

## Build & run

1. Ensure you have JDK 25 setup, including `JAVA_HOME`.
   You may download one from the [Adoptium](https://adoptium.net/) project, or your local package manager.

2. Run the following commands:

   **Linux & macOS**
   ```shell
   git clone https://github.com/maxaltdev/coinplot.git # clone the repo
   cd coinplot # go into the cloned repo
   ./mvnw package -Pproduction # build a self-contained JAR file (this might take a few minutes)
   java -jar ./target/coinplot-3.1.0.jar # run the JAR file on the JRE
   ```

   **Microsoft Windows**
   ```shell
   git clone https://github.com/maxaltdev/coinplot.git # clone the repo
   cd coinplot # go into the cloned repo
   .\mvnw.cmd package -Pproduction # build a self-contained JAR file (this might take a few minutes)
   java -jar .\target\coinplot-3.1.0-dev.jar # run the JAR file on the JRE
   ```

   The resulting JAR file should be fully self-contained and can be copied and ran in any environment where JRE 25 is set up.

> [!IMPORTANT]
> You will need an active [Vaadin Pro](https://vaadin.com/pro) subscription to use the line charts in this web app. 

## Licensing

[MIT license.](LICENSE)

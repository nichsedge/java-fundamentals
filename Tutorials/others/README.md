# E-Banking UI Tutorials (JavaFX)

This directory contains tutorials and assignments built using JavaFX to simulate E-Banking user interfaces.

## Applications Included

### UI_Bank_NI
This application demonstrates a simple login interface for an E-Banking application.
- `Tugasfx.java`: Contains the JavaFX Application to show the primary interface.

### ControlJavaFX
This application demonstrates a more complex interface containing user search, tabs, and tables for displaying banking transactions.
- `Tugasfx.java`: The main JavaFX Application file.
- `DataTransaksi.java`: The data model representing a bank transaction.
- `dataset.txt`: Sample dataset of bank transactions for the application to read.

## Prerequisites

To compile and run these JavaFX applications using modern Java, you must download the JavaFX SDK.

1. Download the correct version of the OpenJFX SDK for your operating system from the [Gluon JavaFX download page](https://gluonhq.com/products/javafx/).
2. Extract the downloaded zip/tar file into a known directory. For this guide, we will assume it is extracted to `/path/to/javafx-sdk`.

## Compiling the Applications

Since JavaFX is no longer bundled with the standard JDK (starting from Java 11), you must specify the module path and the required modules when compiling the code.

### Compiling `UI_Bank_NI`

```bash
cd UI_Bank_NI
javac --module-path /path/to/javafx-sdk/lib --add-modules javafx.controls,javafx.fxml tugas/Tugasfx.java
```

### Compiling `ControlJavaFX`

```bash
cd ControlJavaFX
javac --module-path /path/to/javafx-sdk/lib --add-modules javafx.controls,javafx.fxml tugas/Tugasfx.java tugas/DataTransaksi.java
```

## Running the Applications

Similarly, to run the compiled application, you need to provide the `--module-path` and `--add-modules` arguments to the `java` command.

### Running `UI_Bank_NI`

```bash
cd UI_Bank_NI
java --module-path /path/to/javafx-sdk/lib --add-modules javafx.controls,javafx.fxml tugas.Tugasfx
```

### Running `ControlJavaFX`

```bash
cd ControlJavaFX
java --module-path /path/to/javafx-sdk/lib --add-modules javafx.controls,javafx.fxml tugas.Tugasfx
```

**Note:** For `ControlJavaFX`, make sure the `dataset.txt` file is in the same working directory from which you execute the `java` command, or modify `Tugasfx.java` to point to its absolute path.

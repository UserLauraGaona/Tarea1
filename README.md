# Tarea1

![Captura de pantalla 2024-07-09 151722](https://github.com/UserLauraGaona/Tarea1/assets/175163285/780ba35e-3b4d-49c7-92c4-54a1711a75c3)

Este código de la clase Main define la interfaz gráfica de una aplicación para consultar resultados de Fórmula 1 por año. Utiliza la librería JavaFX para crear los elementos visuales.

Partes del código:
Objetos:
* Se crea una instancia de DriverResultRepository para interactuar con la base de datos y obtener resultados.
* Se define una TableView para mostrar los resultados en una tabla.
* Se crea un ComboBox para que el usuario seleccione el año.
Método start:
* Define el título de la ventana principal ("Formula 1 Results").
ComboBox:
* Se obtienen los años disponibles a través del repositorio (driverResultRepository.getAvailableYears).
* Se llena el ComboBox con los años usando FXCollections.observableArrayList.
* Se define un evento (setOnAction) para el ComboBox que llama al método updateTable cuando se selecciona un año.
TableView:
* Se crean columnas para la tabla con los nombres de las propiedades del objeto DriverResult (nombre del piloto, victorias, puntos totales y ranking).
* Se utiliza setCellValueFactory para asignar cada columna a la propiedad correspondiente del objeto DriverResult.
* Se añaden todas las columnas a la tabla (tableView.getColumns().addAll).
Layout:
* Se crea un contenedor VBox para organizar los elementos de forma vertical con un espacio de 10 pixeles entre ellos.
* Se agrega el ComboBox y la TableView al contenedor VBox.
* Se establece un margen de 10 pixeles para el contenedor.
* Se crea la escena con el contenedor VBox y se define su tamaño (600x400 pixeles).
* Se muestra la ventana principal (primaryStage).
Método updateTable:
* Recibe el año seleccionado por el usuario.
* Obtiene los resultados para ese año a través del repositorio (driverResultRepository.getResultByYear).
* Convierte la lista de resultados en una ObservableList compatible con JavaFX (FXCollections.observableArrayList).
* Actualiza la tabla (tableView) con los nuevos datos.
Método main:
* Inicia la aplicación JavaFX (launch).

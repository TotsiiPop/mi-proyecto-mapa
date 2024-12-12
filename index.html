<?php
// Incluir el archivo de conexión
include('conexion.php');

// Obtener todos los empleados para mostrarlos en la tabla inicial
$sql = "SELECT * FROM Empleados";
$result = $conn->query($sql);
?>

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gestión de Empleados</title>
    <link rel="stylesheet" href="estilos.css">
</head>
<body>
    <div class="container">
        <h1>Gestión de Empleados</h1>

        <!-- Formulario para consultas personalizadas -->
        <h2>Realizar consulta personalizada</h2>
        <form method="POST" action="">
            <label for="consulta">Escribe tu consulta SQL:</label><br>
            <textarea name="consulta" id="consulta" rows="4" cols="50" required></textarea><br>
            <input type="submit" value="Ejecutar consulta">
        </form>

        <!-- Tabla para mostrar los empleados -->
        <h2>Lista de Empleados</h2>
        <table>
            <thead>
                <tr>
                    <th>ID</th>
                    <th>Nombre</th>
                    <th>Apellido</th>
                    <th>Fecha de Nacimiento</th>
                    <th>Fecha de Contratación</th>
                    <th>Posición</th>
                    <th>Departamento</th>
                </tr>
            </thead>
            <tbody>
                <?php
                // Mostrar cada empleado en una fila
                if ($result->num_rows > 0) {
                    while ($row = $result->fetch_assoc()) {
                        echo "<tr>
                                <td>{$row['EmpleadoID']}</td>
                                <td>{$row['Nombre']}</td>
                                <td>{$row['Apellido']}</td>
                                <td>{$row['FechaNacimiento']}</td>
                                <td>{$row['FechaContratacion']}</td>
                                <td>{$row['Posicion']}</td>
                                <td>{$row['DepartamentoID']}</td>
                              </tr>";
                    }
                } else {
                    echo "<tr><td colspan='7'>No se encontraron empleados</td></tr>";
                }
                ?>
            </tbody>
        </table>

        <!-- Mostrar resultado de la consulta personalizada -->
        <?php
        if ($_SERVER["REQUEST_METHOD"] == "POST") {
            $consulta = $_POST['consulta'];

            // Validar que no sea una consulta peligrosa
            $prohibido = ['DROP', 'DELETE', 'TRUNCATE'];
            foreach ($prohibido as $palabra) {
                if (stripos($consulta, $palabra) !== false) {
                    echo "<p style='color: red;'>Consulta no permitida: No puedes usar comandos de eliminación o alteración.</p>";
                    exit;
                }
            }

            // Ejecutar la consulta y mostrar los resultados
            $resultadoConsulta = $conn->query($consulta);

            if ($resultadoConsulta) {
                if ($resultadoConsulta->num_rows > 0) {
                    echo "<h2>Resultado de la consulta:</h2>";
                    echo "<table><thead><tr>";

                    // Mostrar encabezados de la consulta
                    $columns = $resultadoConsulta->fetch_fields();
                    foreach ($columns as $column) {
                        echo "<th>{$column->name}</th>";
                    }
                    echo "</tr></thead><tbody>";

                    // Mostrar datos de la consulta
                    while ($fila = $resultadoConsulta->fetch_assoc()) {
                        echo "<tr>";
                        foreach ($fila as $valor) {
                            echo "<td>{$valor}</td>";
                        }
                        echo "</tr>";
                    }
                    echo "</tbody></table>";
                } else {
                    echo "<p>No se encontraron resultados para la consulta.</p>";
                }
            } else {
                echo "<p style='color: red;'>Error en la consulta: " . $conn->error . "</p>";
            }
        }

        // Cerrar la conexión
        $conn->close();
        ?>
    </div>
</body>
</html>

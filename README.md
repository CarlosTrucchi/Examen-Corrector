# Examen-Corrector
Para la Corrección de Parciales de Matemática I - 2025
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Corrector de Examen</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            background-color: #f0f2f5;
            padding: 20px;
        }
        .container {
            background: #fff;
            padding: 25px 40px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
            width: 100%;
            max-width: 800px;
            margin-bottom: 20px;
        }
        h1 {
            color: #004d40;
            margin-bottom: 5px;
        }
        h2 {
            color: #555;
            font-size: 1.2em;
            margin-top: 0;
            margin-bottom: 20px;
        }
        .section-title {
            background-color: #e0f2f1;
            padding: 10px;
            border-radius: 5px;
            margin-bottom: 15px;
            color: #004d40;
            font-weight: bold;
        }
        .student-info {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-bottom: 20px;
        }
        .student-info input {
            padding: 8px;
            border-radius: 5px;
            border: 1px solid #ccc;
            width: 100%;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-bottom: 20px;
        }
        th, td {
            border: 1px solid #ccc;
            padding: 10px;
            text-align: center;
            vertical-align: middle;
        }
        th {
            background-color: #e0f2f1;
            color: #004d40;
        }
        tr:nth-child(even) {
            background-color: #f9f9f9;
        }
        button {
            padding: 12px 25px;
            font-size: 16px;
            color: #fff;
            background-color: #00796b;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 20px;
            transition: background-color 0.3s ease;
        }
        button:hover {
            background-color: #004d40;
        }
        .results {
            margin-top: 30px;
            padding: 15px;
            background-color: #e8f5e9;
            border: 1px solid #c8e6c9;
            border-radius: 5px;
            font-size: 1.2em;
            font-weight: bold;
            color: #2e7d32;
            display: none;
        }
        #resultTable {
            margin-top: 40px;
        }
        #resultTable th, #resultTable td {
            font-size: 0.9em;
        }
        #editable-title {
            cursor: pointer;
            border-bottom: 1px dashed #004d40;
        }
        .confirm-btn {
            padding: 8px 15px;
            margin-top: 0;
            background-color: #2e7d32;
        }
        .confirm-btn:hover {
            background-color: #1b5e20;
        }
        .dni-container {
            display: flex;
            gap: 10px;
            align-items: center;
        }
        .info-field-group {
            display: flex;
            flex-direction: column;
        }
        .file-upload-container {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Primer Parcial de Matemática II - <span id="editable-title" onclick="makeEditable(this)">TEMA 1</span></h1>
    <h2>Redictado 2025</h2>

    <div class="section-title">1. Configurar Clave de Respuestas</div>
    <div id="key-section">
        <table>
            <thead>
                <tr>
                    <th></th>
                    <th>1</th><th>2</th><th>3</th><th>4</th><th>5</th><th>6</th><th>7</th><th>8</th><th>9</th><th>10</th>
                </tr>
            </thead>
            <tbody>
                <tr><td>a</td><td><input type="radio" name="key-q1" value="a"></td><td><input type="radio" name="key-q2" value="a"></td><td><input type="radio" name="key-q3" value="a"></td><td><input type="radio" name="key-q4" value="a"></td><td><input type="radio" name="key-q5" value="a"></td><td><input type="radio" name="key-q6" value="a"></td><td><input type="radio" name="key-q7" value="a"></td><td><input type="radio" name="key-q8" value="a"></td><td><input type="radio" name="key-q9" value="a"></td><td><input type="radio" name="key-q10" value="a"></td></tr>
                <tr><td>b</td><td><input type="radio" name="key-q1" value="b"></td><td><input type="radio" name="key-q2" value="b"></td><td><input type="radio" name="key-q3" value="b"></td><td><input type="radio" name="key-q4" value="b"></td><td><input type="radio" name="key-q5" value="b"></td><td><input type="radio" name="key-q6" value="b"></td><td><input type="radio" name="key-q7" value="b"></td><td><input type="radio" name="key-q8" value="b"></td><td><input type="radio" name="key-q9" value="b"></td><td><input type="radio" name="key-q10" value="b"></td></tr>
                <tr><td>c</td><td><input type="radio" name="key-q1" value="c"></td><td><input type="radio" name="key-q2" value="c"></td><td><input type="radio" name="key-q3" value="c"></td><td><input type="radio" name="key-q4" value="c"></td><td><input type="radio" name="key-q5" value="c"></td><td><input type="radio" name="key-q6" value="c"></td><td><input type="radio" name="key-q7" value="c"></td><td><input type="radio" name="key-q8" value="c"></td><td><input type="radio" name="key-q9" value="c"></td><td><input type="radio" name="key-q10" value="c"></td></tr>
                <tr><td>d</td><td><input type="radio" name="key-q1" value="d"></td><td><input type="radio" name="key-q2" value="d"></td><td><input type="radio" name="key-q3" value="d"></td><td><input type="radio" name="key-q4" value="d"></td><td><input type="radio" name="key-q5" value="d"></td><td><input type="radio" name="key-q6" value="d"></td><td><input type="radio" name="key-q7" value="d"></td><td><input type="radio" name="key-q8" value="d"></td><td><input type="radio" name="key-q9" value="d"></td><td><input type="radio" name="key-q10" value="d"></td></tr>
                <tr><td>e</td><td><input type="radio" name="key-q1" value="e"></td><td><input type="radio" name="key-q2" value="e"></td><td><input type="radio" name="key-q3" value="e"></td><td><input type="radio" name="key-q4" value="e"></td><td><input type="radio" name="key-q5" value="e"></td><td><input type="radio" name="key-q6" value="e"></td><td><input type="radio" name="key-q7" value="e"></td><td><input type="radio" name="key-q8" value="e"></td><td><input type="radio" name="key-q9" value="e"></td><td><input type="radio" name="key-q10" value="e"></td></tr>
                <tr><td>vacío</td><td><input type="radio" name="key-q1" value="vacio"></td><td><input type="radio" name="key-q2" value="vacio"></td><td><input type="radio" name="key-q3" value="vacio"></td><td><input type="radio" name="key-q4" value="vacio"></td><td><input type="radio" name="key-q5" value="vacio"></td><td><input type="radio" name="key-q6" value="vacio"></td><td><input type="radio" name="key-q7" value="vacio"></td><td><input type="radio" name="key-q8" value="vacio"></td><td><input type="radio" name="key-q9" value="vacio"></td><td><input type="radio" name="key-q10" value="vacio"></td></tr>
            </tbody>
        </table>
        <button onclick="saveKey()">Guardar Clave</button>
        <p id="keyStatus" style="color:red; margin-top:10px;">¡Debes configurar la clave de respuestas primero!</p>
    </div>
</div>

<div class="container">
    <div class="section-title">2. Cargar Datos del Alumno y Corregir</div>
    
    <div class="file-upload-container">
        <label for="excelFile">Cargar lista de alumnos (Excel):</label>
        <input type="file" id="excelFile" accept=".xlsx, .xls">
        <button id="uploadButton" onclick="cargarExcel()">Cargar Archivo</button>
    </div>
    <p id="excelStatus" style="margin-top: 10px; color: red;">No se ha cargado ningún archivo de Excel.</p>

    <div class="student-info">
        <div class="info-field-group">
            <label for="dni">DNI:</label>
            <div class="dni-container">
                <input type="text" id="dni" pattern="[0-9]{8}" maxlength="8">
                <button class="confirm-btn" onclick="buscarAlumno()">Confirmar</button>
            </div>
        </div>
        <div class="info-field-group">
            <label for="apellidoNombre">Apellido y Nombre:</label>
            <input type="text" id="apellidoNombre" readonly>
        </div>
        <div class="info-field-group">
            <label for="comision">Comisión:</label>
            <input type="text" id="comision" readonly>
        </div>
        <div class="info-field-group">
            <label for="numeroAlumno">Número de Alumno:</label>
            <input type="text" id="numeroAlumno" readonly>
        </div>
        <div class="info-field-group">
            <label for="aula">Aula en que Rindió:</label>
            <input type="text" id="aula" readonly>
        </div>
        <div class="info-field-group">
            <label for="profesorApellido">Apellido del Profesor:</label>
            <input type="text" id="profesorApellido">
        </div>
    </div>

    <h3>Grilla de Respuestas</h3>
    <table>
        <thead>
            <tr>
                <th></th>
                <th>1</th><th>2</th><th>3</th><th>4</th><th>5</th><th>6</th><th>7</th><th>8</th><th>9</th><th>10</th>
            </tr>
        </thead>
        <tbody>
            <tr><td>a</td><td><input type="radio" name="student-q1" value="a"></td><td><input type="radio" name="student-q2" value="a"></td><td><input type="radio" name="student-q3" value="a"></td><td><input type="radio" name="student-q4" value="a"></td><td><input type="radio" name="student-q5" value="a"></td><td><input type="radio" name="student-q6" value="a"></td><td><input type="radio" name="student-q7" value="a"></td><td><input type="radio" name="student-q8" value="a"></td><td><input type="radio" name="student-q9" value="a"></td><td><input type="radio" name="student-q10" value="a"></td></tr>
            <tr><td>b</td><td><input type="radio" name="student-q1" value="b"></td><td><input type="radio" name="student-q2" value="b"></td><td><input type="radio" name="student-q3" value="b"></td><td><input type="radio" name="student-q4" value="b"></td><td><input type="radio" name="student-q5" value="b"></td><td><input type="radio" name="student-q6" value="b"></td><td><input type="radio" name="student-q7" value="b"></td><td><input type="radio" name="student-q8" value="b"></td><td><input type="radio" name="student-q9" value="b"></td><td><input type="radio" name="student-q10" value="b"></td></tr>
            <tr><td>c</td><td><input type="radio" name="student-q1" value="c"></td><td><input type="radio" name="student-q2" value="c"></td><td><input type="radio" name="student-q3" value="c"></td><td><input type="radio" name="student-q4" value="c"></td><td><input type="radio" name="student-q5" value="c"></td><td><input type="radio" name="student-q6" value="c"></td><td><input type="radio" name="student-q7" value="c"></td><td><input type="radio" name="student-q8" value="c"></td><td><input type="radio" name="student-q9" value="c"></td><td><input type="radio" name="student-q10" value="c"></td></tr>
            <tr><td>d</td><td><input type="radio" name="student-q1" value="d"></td><td><input type="radio" name="student-q2" value="d"></td><td><input type="radio" name="student-q3" value="d"></td><td><input type="radio" name="student-q4" value="d"></td><td><input type="radio" name="student-q5" value="d"></td><td><input type="radio" name="student-q6" value="d"></td><td><input type="radio" name="student-q7" value="d"></td><td><input type="radio" name="student-q8" value="d"></td><td><input type="radio" name="student-q9" value="d"></td><td><input type="radio" name="student-q10" value="d"></td></tr>
            <tr><td>e</td><td><input type="radio" name="student-q1" value="e"></td><td><input type="radio" name="student-q2" value="e"></td><td><input type="radio" name="student-q3" value="e"></td><td><input type="radio" name="student-q4" value="e"></td><td><input type="radio" name="student-q5" value="e"></td><td><input type="radio" name="student-q6" value="e"></td><td><input type="radio" name="student-q7" value="e"></td><td><input type="radio" name="student-q8" value="e"></td><td><input type="radio" name="student-q9" value="e"></td><td><input type="radio" name="student-q10" value="e"></td></tr>
            <tr><td>vacío</td><td><input type="radio" name="student-q1" value="vacio"></td><td><input type="radio" name="student-q2" value="vacio"></td><td><input type="radio" name="student-q3" value="vacio"></td><td><input type="radio" name="student-q4" value="vacio"></td><td><input type="radio" name="student-q5" value="vacio"></td><td><input type="radio" name="student-q6" value="vacio"></td><td><input type="radio" name="student-q7" value="vacio"></td><td><input type="radio" name="student-q8" value="vacio"></td><td><input type="radio" name="student-q9" value="vacio"></td><td><input type="radio" name="student-q10" value="vacio"></td></tr>
            </tbody>
    </table>
    
    <button onclick="checkAnswers()">Corregir y Cargar</button>
    <div id="results" class="results"></div>
</div>

<div class="container">
    <div class="section-title">3. Listado de Alumnos y Exportar</div>
    <div style="text-align: right; margin-bottom: 10px;">
        <button onclick="exportToCsv()">Exportar a Excel (CSV)</button>
    </div>
    <table id="resultTable">
        <thead>
            <tr>
                <th>Alumno</th>
                <th>DNI</th>
                <th>Correctas</th>
                <th>Incorrectas</th>
                <th>Nota</th>
                <th>Calificación</th>
                <th>Profesor</th>
            </tr>
        </thead>
        <tbody>
            </tbody>
    </table>
</div>

<script src="https://cdn.jsdelivr.net/npm/read-excel-file@5.0.0/dist/read-excel-file.min.js"></script>

<script>
    let correctAnswers = null;
    let studentsResults = [];
    let studentsFromExcel = [];

    function makeEditable(element) {
        const text = element.textContent;
        const input = document.createElement('input');
        input.type = 'text';
        input.value = text;
        input.style.border = '1px solid #ccc';
        input.style.fontSize = '1em';
        input.style.textAlign = 'center';
        input.style.width = '100px';
        input.onblur = function() {
            element.textContent = this.value;
            element.classList.remove('editing');
        };
        input.onkeydown = function(e) {
            if (e.key === 'Enter') {
                this.blur();
            }
        };
        element.textContent = '';
        element.appendChild(input);
        input.focus();
    }

    function displayStudentData() {
        const tableBody = document.querySelector('#resultTable tbody');
        tableBody.innerHTML = '';
        studentsResults.forEach(student => {
            const row = tableBody.insertRow();
            row.innerHTML = `
                <td>${student.name}</td>
                <td>${student.dni}</td>
                <td>${student.correctas}</td>
                <td>${student.incorrectas}</td>
                <td>${student.nota}</td>
                <td>${student.calificacion}</td>
                <td>${student.profesor}</td>
            `;
        });
    }

    function saveKey() {
        const key = {};
        let allQuestionsAnswered = true;
        for (let i = 1; i <= 10; i++) {
            const selected = document.querySelector(`input[name="key-q${i}"]:checked`);
            if (selected) {
                key[`q${i}`] = selected.value;
            } else {
                allQuestionsAnswered = false;
                break;
            }
        }
        if (allQuestionsAnswered) {
            correctAnswers = key;
            document.getElementById('keyStatus').textContent = '✅ Clave de respuestas guardada correctamente.';
            document.getElementById('keyStatus').style.color = 'green';
            alert('¡Clave guardada con éxito! Ahora puedes corregir los exámenes.');
        } else {
            document.getElementById('keyStatus').textContent = '⚠️ Por favor, marca todas las respuestas de la clave.';
            document.getElementById('keyStatus').style.color = 'red';
        }
    }

    function checkAnswers() {
        if (!correctAnswers) {
            alert('Error: Por favor, guarda la clave de respuestas primero.');
            return;
        }

        const professor = document.getElementById('profesorApellido').value;
        const studentName = document.getElementById('apellidoNombre').value;
        const studentDNI = document.getElementById('dni').value;
        const dniInput = document.getElementById('dni');
        const studentComision = document.getElementById('comision').value;
        const studentNumero = document.getElementById('numeroAlumno').value;
        const studentAula = document.getElementById('aula').value;

        if (!studentName || !studentDNI || !professor || !studentComision || !studentNumero || !studentAula) {
            alert('Por favor, completa todos los campos de información del alumno y profesor. Puedes usar el botón "Confirmar" después de ingresar el DNI para autocompletar.');
            return;
        }
        if (!dniInput.checkValidity()) {
            alert('El DNI debe contener exactamente 8 dígitos numéricos.');
            return;
        }

        let correctCount = 0;
        let incorrectCount = 0;
        let blankCount = 0;

        for (let i = 1; i <= 10; i++) {
            const selected = document.querySelector(`input[name="student-q${i}"]:checked`);
            const correctAnswer = correctAnswers[`q${i}`];
            if (!selected) {
                incorrectCount++;
            } else if (selected.value === 'vacio') {
                blankCount++;
            } else if (selected.value === correctAnswer) {
                correctCount++;
            } else {
                incorrectCount++;
            }
        }

        let finalNote = 0;
        let status = '';
        if (correctCount >= 5) {
            status = 'Aprobado';
        } else {
            status = 'Desaprobado';
        }
        
        if (correctCount <= 1) finalNote = 1;
        else if (correctCount === 2) finalNote = 2;
        else if (correctCount <= 4) finalNote = 3;
        else if (correctCount === 5) finalNote = 4;
        else if (correctCount === 6) finalNote = 6;
        else if (correctCount === 7) finalNote = 7;
        else if (correctCount === 8) finalNote = 8;
        else if (correctCount === 9) finalNote = 9;
        else if (correctCount === 10) finalNote = 10;

        const resultsDiv = document.getElementById('results');
        resultsDiv.innerHTML = `
            <p><strong>Alumno:</strong> ${studentName} - DNI: ${studentDNI}</p>
            <p><strong>Correctas:</strong> ${correctCount} | <strong>Incorrectas:</strong> ${incorrectCount} | <strong>En blanco:</strong> ${blankCount}</p>
            <p><strong>Nota:</strong> ${finalNote} | <strong>Calificación:</strong> ${status}</p>
        `;
        resultsDiv.style.display = 'block';

        studentsResults.push({
            name: studentName,
            dni: studentDNI,
            comision: studentComision,
            numero: studentNumero,
            aula: studentAula,
            correctas: correctCount,
            incorrectas: incorrectCount,
            nota: finalNote,
            calificacion: status,
            profesor: professor
        });

        displayStudentData();

        document.getElementById('profesorApellido').value = '';
        document.getElementById('dni').value = '';
        document.getElementById('apellidoNombre').value = '';
        document.getElementById('comision').value = '';
        document.getElementById('numeroAlumno').value = '';
        document.getElementById('aula').value = '';
        
        const radioButtons = document.querySelectorAll('input[name^="student-"]:checked');
        radioButtons.forEach(radio => radio.checked = false);
    }

    function exportToCsv() {
        if (studentsResults.length === 0) {
            alert('No hay datos para exportar. Primero corrige y carga algunos exámenes.');
            return;
        }

        let csvContent = "data:text/csv;charset=utf-8,";
        const headers = ["LEGAJO", "NOMBRE", "COMISION", "NOTA", "CORREGIDO", "AULA"];
        csvContent += headers.join(",") + "\r\n";

        studentsResults.forEach(student => {
            const row = [
                `"${student.dni}"`,
                `"${student.name}"`,
                `"${student.comision}"`,
                student.nota,
                `"${student.profesor}"`,
                `"${student.aula}"`
            ];
            csvContent += row.join(",") + "\r\n";
        });

        const encodedUri = encodeURI(csvContent);
        const link = document.createElement("a");
        link.setAttribute("href", encodedUri);
        link.setAttribute("download", "resultados_examen.csv");
        document.body.appendChild(link);
        link.click();
        document.body.removeChild(link);
    }

    function cargarExcel() {
        const fileInput = document.getElementById('excelFile');
        const file = fileInput.files[0];
        const excelStatus = document.getElementById('excelStatus');

        if (!file) {
            excelStatus.textContent = '⚠️ Por favor, selecciona un archivo de Excel primero.';
            excelStatus.style.color = 'red';
            return;
        }
        
        excelStatus.textContent = 'Cargando archivo, por favor espera...';
        excelStatus.style.color = 'orange';

        readXlsxFile(file).then((rows) => {
            // Se asume la siguiente estructura de columnas: DNI, Comisión, Número de Alumno, Apellido y Nombre, Aula.
            studentsFromExcel = rows.slice(1).map(row => ({
                dni: String(row[0]),       
                comision: row[1],          
                numero: String(row[2]),    
                name: row[3],              
                aula: row[4]               
            }));
            excelStatus.textContent = '✅ Archivo Excel cargado con éxito. Ya puedes buscar por DNI.';
            excelStatus.style.color = 'green';
            alert('¡Lista de alumnos cargada! Ya puedes buscar por DNI.');
        }).catch(error => {
            excelStatus.textContent = `⚠️ Error al leer el archivo. Asegúrate de que el formato sea válido. Detalles: ${error.message}`;
            excelStatus.style.color = 'red';
            console.error(error);
        });
    }

    function buscarAlumno() {
        const dniIngresado = document.getElementById('dni').value.trim();

        if (studentsFromExcel.length === 0) {
            alert('Primero debes cargar un archivo Excel con la lista de alumnos usando el botón "Cargar Archivo".');
            return;
        }

        if (dniIngresado.length !== 8) {
            alert('Por favor, ingresa un DNI de 8 dígitos.');
            document.getElementById('apellidoNombre').value = '';
            document.getElementById('comision').value = '';
            document.getElementById('numeroAlumno').value = '';
            document.getElementById('aula').value = '';
            return;
        }

        const alumnoEncontrado = studentsFromExcel.find(alumno => alumno.dni === dniIngresado);

        if (alumnoEncontrado) {
            document.getElementById('apellidoNombre').value = alumnoEncontrado.name;
            document.getElementById('comision').value = alumnoEncontrado.comision;
            document.getElementById('numeroAlumno').value = alumnoEncontrado.numero;
            document.getElementById('aula').value = alumnoEncontrado.aula;
        } else {
            document.getElementById('apellidoNombre').value = '';
            document.getElementById('comision').value = '';
            document.getElementById('numeroAlumno').value = '';
            document.getElementById('aula').value = '';
            alert('DNI no encontrado en el archivo Excel. Por favor, verifica el número.');
        }
    }
</script>
    </body>
</html>

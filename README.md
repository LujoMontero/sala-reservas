🏢 API de Reservas de Salas – Testing Ágil con TDD

Este proyecto es una API simple para gestionar reservas de salas en una oficina. Fue desarrollado aplicando Agile Testing, TDD (Test-Driven Development) y se integra en un flujo CI/CD con GitHub Actions.

🚀 Objetivos del Proyecto

✅ Aplicar los principios de Testing Ágil y TDD✅ Diseñar una API con Flask✅ Crear pruebas unitarias e integración desde el inicio✅ Automatizar la ejecución de pruebas✅ Integrar pruebas en GitHub Actions

⚙️ Requisitos

Python 3.10+

Git

pip

💪 Instalación y Configuración

1. Clona el repositorio

git clone https://github.com/LujoMontero/sala-reservas
cd sala-reservas

2. Crea y activa un entorno virtual

python -m venv venv
# En Windows
venv\Scripts\activate
# En Linux/Mac
source venv/bin/activate

3. Instala las dependencias

pip install -r requirements.txt

📁 Estructura del Proyecto

sala-reservas/
├── app/
│   ├── __init__.py
│   ├── api.py
│   └── reservas.py
├── tests/
│   ├── test_api.py
│   └── test_reservas.py
├── requirements.txt
└── .github/
    └── workflows/
        └── testing.yml

▶️ Ejecutar la API

Solo si quieres probarla manualmente:

python app/api.py

Luego puedes hacer un POST a http://localhost:5000/reservar con JSON:

{
  "sala": "A",
  "hora": "10:00"
}

✅ Ejecutar las Pruebas

Desde la raíz del proyecto:

pytest

Esto ejecutará:

Pruebas unitarias (test_reservas.py)

Pruebas de integración (test_api.py)

🔁 Automatización con GitHub Actions

El archivo .github/workflows/testing.yml ejecuta automáticamente las pruebas en cada push o pull_request.

⚖️ Configuración Clave:

- name: Ejecutar pruebas
  run: |
    source venv/bin/activate
    export PYTHONPATH=.
    pytest

❗ Solución al error ModuleNotFoundError: No module named 'app'

Ese error se soluciona con:

export PYTHONPATH=.

Esto le indica a Python que el directorio actual (.) es la raíz de los módulos.

💡 Pruebas Cubiertas

✅ Unitarias (tests/test_reservas.py)

Verifica si una sala está disponible o no en una hora dada.

✅ Integración (tests/test_api.py)

Simula solicitudes HTTP a la API (POST /reservar) y valida las respuestas.

🤔 Reflexión Final

Agile Testing permite entregar calidad desde el día 1.

TDD nos obliga a pensar primero en los requisitos y el comportamiento.

Automatizar con GitHub Actions ahorra tiempo y previene errores humanos.
![Captura de pantalla 2025-06-17 124255](https://github.com/user-attachments/assets/fcee6902-5c7c-4782-957c-f6e73889dbf0)
![Captura de pantalla 2025-06-17 124435](https://github.com/user-attachments/assets/31f20898-267e-4429-b495-964490fdb249)
![Captura de pantalla 2025-06-17 185836](https://github.com/user-attachments/assets/5c385ee5-ce1a-4339-a407-39aaac308bee)
![Captura de pantalla 2025-06-17 185859](https://github.com/user-attachments/assets/050f6248-3abd-43d8-ab43-2a21049dbb63)
![Captura de pantalla 2025-06-17 190122](https://github.com/user-attachments/assets/e1a18959-0b6b-4880-bacb-541624cead8a)

✍️ Autor

Nombre: Luis Montero

Proyecto educativo: Módulo 4 – Automatización de Pruebas Ágiles

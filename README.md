# [Nombre del Proyecto: Simulador de Gestor de Procesos]

[Escribe aquí una breve descripción del proyecto en 1 o 2 líneas. Ejemplo: Un simulador educativo y de alto rendimiento que modela la planificación de procesos, asignación de memoria RAM y concurrencia con semáforos en sistemas operativos.]

---

## 📚 Información del Curso

* **Materia:** Sistemas Operativos
* **Institución:** [Nombre de tu Universidad o Institución]
* **Semestre:** [Ejemplo: Sexto Semestre - 2026]
* **Profesor(es):** [Nombre del Profesor o Profesores]

---

## 👥 Integrantes del Equipo

* **Integrante 1:** [Tu Nombre completo] - [Matrícula/ID]
* **Integrante 2:** [Nombre completo] - [Matrícula/ID]
* **Integrante 3:** [Nombre completo] - [Matrícula/ID]

---

## 🚀 Requisitos e Instalación

Este simulador está desarrollado en **Python 3** utilizando la librería gráfica moderna **CustomTkinter**.

### 1. Clonar el repositorio
```bash
git clone https://github.com/[tu-usuario]/simulador-gestor-procesos.git
cd simulador-gestor-procesos
```

### 2. Crear y activar entorno virtual (Recomendado)
```bash
# En Windows
python -m venv venv
.\venv\Scripts\activate

# En macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Instalar dependencias
```bash
pip install -r requirements.txt
```

### 4. Ejecutar el Simulador
```bash
python src/main.py
```

---

## 📂 Estructura del Proyecto

El repositorio está estructurado siguiendo la propuesta de arquitectura académica para la materia de Sistemas Operativos:

```text
simulador-gestor-procesos/
├── README.md               # Este archivo de documentación
├── LICENSE                 # Licencia de uso del software (MIT)
├── requirements.txt        # Dependencias de Python
├── .gitignore              # Archivos excluidos de git
├── src/                    # Código fuente
│   ├── main.py             # Punto de entrada
│   ├── core/               # Núcleo del Sistema Operativo
│   │   ├── process.py      # Estructura del PCB y estados de procesos
│   │   ├── scheduler.py    # Algoritmos de Planificación (FCFS, SJF, RR, Prioridad)
│   │   ├── resource.py     # Gestor de recursos (CPU, memoria RAM)
│   │   └── generator.py    # Generador automático de procesos
│   ├── ipc/                # Comunicación entre procesos (IPC)
│   │   ├── semaphore.py    # Abstracción de Semáforos y Mutex
│   │   ├── channel.py      # Memoria Compartida / Buffer
│   │   └── conflict_simulation.py # Simulación Productor-Consumidor (Sincronizado vs Inseguro)
│   └── ui/                 # Interfaz de Usuario
│       ├── gui.py          # Dashboard Gráfico Premium (CustomTkinter)
│       └── logger.py       # Bitácora / Consola del sistema
├── tests/                  # Pruebas de integración unitarias
│   ├── scheduler_tests.py  # Tests de los planificadores
│   ├── resource_tests.py   # Tests del administrador de recursos
│   └── ipc_tests.py        # Tests del flujo sincronizado de IPC
├── examples/               # Casos de uso demostrativos y scripts
│   ├── productor_consumidor.py
│   └── round_robin_demo.py
├── docs/                   # Documentación adicional y PDFs
└── capturas/               # Capturas de pantalla de la aplicación
```

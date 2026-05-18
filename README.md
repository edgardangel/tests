# Simulador de gestor de procesos para Sistemas Operativos

Un simulador interactivo y didáctico desarrollado en Python que modela en tiempo real la planificación de CPU (FCFS, SJF, RR y Prioridades), el control de recursos (memoria RAM limitada) y la sincronización de procesos colaboradores mediante memoria compartida, semáforos y mutex.

---

## 📚 Información del Curso

* **Materia:** Sistemas Operativos
* **Institución:** Universidad Autónoma de Tamaulipas
* **Semestre:** Semestre 2026-1
* **Profesor:** Muñoz Quintero Dante Adolfo

---

## 👥 Integrantes del Equipo

* **Del Angel Del Angel Edgar**
* **Hipolito Perez Silvestre Abraham**

---

## 🚀 Requisitos e Instalación

Este simulador está desarrollado en **Python 3** utilizando la librería gráfica moderna **CustomTkinter**.

### 1. Clonar el repositorio
```bash
git clone https://github.com/edgardangel/simulador-gestor-procesos.git
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

El repositorio está estructurado siguiendo la propuesta de arquitectura académica para la materia de Sistemas Operativos, traducida y optimizada a Python:

```text
simulador-gestor-procesos/
├── .github/
│   └── workflows/
│       └── python-app.yml     # Pipeline de Integración Continua (CI/CD)
├── benches/
│   └── scheduler_bench.py      # Benchmark automatizado de rendimiento de algoritmos
├── capturas/                   # Screenshots del simulador (ejecución y concurrencia)
│   ├── .gitkeep
│   └── *.png                   # 9 Capturas de pantalla de demostración
├── docs/                       # Manuales y documentación académica
│   ├── .gitkeep
│   ├── reporte_tecnico_completo.md # Borrador de manual en Markdown con normas APA
│   └── Entregable_proyecto_gestor_procesos.pdf # Entregable oficial del proyecto
├── examples/                   # Casos de uso demostrativos y scripts CLI
│   ├── productor_consumidor.py # Demostración simple Productor-Consumidor
│   └── round_robin_demo.py     # Demostración CLI interactiva de Round Robin
├── src/                        # Código fuente principal de la aplicación
│   ├── __init__.py             # Inicializador de paquete de src
│   ├── main.py                 # Punto de entrada ejecutable
│   ├── core/                   # Núcleo del Sistema Operativo simulado
│   │   ├── __init__.py
│   │   ├── generator.py        # Generador de procesos en caliente y por lotes
│   │   ├── process.py          # Bloque de Control de Procesos (PCB) y transiciones
│   │   ├── resource.py         # Pool de memoria RAM física con exclusión mutua
│   │   └── scheduler.py        # Estrategias FCFS, SJF, Prioridades y Round Robin
│   ├── ipc/                    # Mecanismos de comunicación interprocesos
│   │   ├── __init__.py
│   │   ├── channel.py          # Canal de memoria compartida para mensajes (buffer circular)
│   │   ├── conflict_simulation.py # Simulación multihilo (Modo Seguro vs Inseguro)
│   │   └── semaphore.py        # Primitivas didácticas de Semáforos y Mutex
│   └── ui/                     # Componentes de visualización gráfica
│       ├── __init__.py
│       ├── gui.py              # Interfaz gráfica moderna en CustomTkinter
│       └── logger.py           # Bitácora thread-safe e intermediario asíncrono
├── tests/                      # Batería de pruebas de integración unitarias
│   ├── __init__.py
│   ├── ipc_tests.py            # Validación de semáforos, mutex y colisiones
│   ├── resource_tests.py       # Validación de exclusión mutua y límites de RAM
│   └── scheduler_tests.py      # Validación del ordenamiento y quantum de despachadores
├── .gitignore                  # Patrones de exclusión profesionales de Git para Python
├── LICENSE                     # Licencia académica MIT
├── README.md                   # Este manual y documentación del proyecto
└── requirements.txt            # Dependencias del proyecto (CustomTkinter)
```

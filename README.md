
# Sistema de Reservas de Hotel - Testing Pack

## Estructura del Proyecto

```
├── app
│   ├── static
│   │   └── style.css
│   ├── templates
│   │   ├── base.html
│   │   ├── booking.html
│   │   ├── index.html
│   │   ├── login.html
│   │   ├── register.html
│   │   └── search_results.html
│   ├── app.py
│   ├── db.py
│   └── init_db.py
├── docs
│   ├── IEEE829_Plan_Template.md
│   ├── Matriz_Riesgo_RPN.xlsx
│   ├── Matriz_Trazabilidad.xlsx
│   └── Plan_Pruebas_Hotel.md
├── metrics
│   ├── dashboards
│   │   ├── dashboard_metricas.html
│   │   └── metricas_resumen.json
│   ├── figs
│   │   ├── semaforo.png
│   │   ├── severity.png
│   │   ├── status.png
│   │   └── trend.png
│   ├── dataset_defectos.csv
│   ├── dataset_defectos_backup.csv
│   ├── mejorar_dataset.py
│   └── sistema_metricas.py
├── tests
│   ├── pytest.ini
│   └── test_app.py
├── README.md
├── hotel_reservas.db
├── requirements.txt
└── run_app.bat
```

---

## Instalación

### 1. Requisitos Previos

- Python 3.8 o superior
- pip (gestor de paquetes de Python)
- Git (opcional)

### 2. Clonar o Descargar el Proyecto

```bash
cd c:\laragon\www\hotel_testing_pack
```

### 3. Crear Entorno Virtual (Recomendado)

```bash
# Windows
python -m venv venv
venv\Scriptsctivate

# Linux/Mac
python3 -m venv venv
source venv/bin/activate
```

### 4. Instalar Dependencias

```bash
pip install -r requirements.txt
```

**Contenido de `requirements.txt`:**

```
Flask==2.3.0
Werkzeug==2.3.0
pytest==7.4.0
pytest-cov==4.1.0
pandas==2.0.0
numpy==1.24.0
matplotlib==3.7.0
```

### 5. Inicializar Base de Datos

```bash
python app/init_db.py
```

Debe ver el mensaje:

```
DB inicializada en: C:\laragon\www\hotel_testing_pack\hotel_reservas.db
Base de datos inicializada correctamente.
```

---

## Uso

### Ejecutar la Aplicación

```bash
# Método 1: Directamente con Python
python app/app.py

# Método 2: Con Flask CLI
set FLASK_APP=app/app.py
set FLASK_ENV=development
flask run

# Método 3: Usar el batch file (Windows)
run_app.bat
```

La aplicación estará disponible en: **http://localhost:5000**

### Flujo de Usuario

1. **Registrarse**: http://localhost:5000/register
2. **Iniciar Sesión**: http://localhost:5000/login
3. **Buscar Habitaciones**: En la página principal
4. **Hacer Reserva**: Seleccionar habitación disponible
5. **Pagar**: Confirmar pago simulado
6. **Cerrar Sesión**: Hacer clic en "Cerrar sesión"

---

## Sistema de Métricas

### Ejecutar el Sistema de Métricas

```bash
cd metrics
python sistema_metricas.py
```

### Sistema

**Imagen 1: Ingreso de habitación**

![Ingreso de habitación]<img width="781" height="392" alt="image" src="https://github.com/user-attachments/assets/b5f03be2-e402-4e64-9c80-fbcfe76e0abc" />


**Imagen 2: Registro de habitación**

![Registro de habitación]<img width="755" height="345" alt="image" src="https://github.com/user-attachments/assets/09b4674a-55eb-4eda-a00f-858ed04793a6" />


**Imagen 3: Pago**

![Pago]<img width="603" height="111" alt="image" src="https://github.com/user-attachments/assets/64e11f95-24e4-47c9-8038-dc724dc5216b" />


**Imagen 4: Registro**

![Registro] <img width="812" height="386" alt="image" src="https://github.com/user-attachments/assets/bea45835-fd2b-4a5c-906b-fa70e04fb0ba" />


**Imagen 5: Inicio de sesión**

![Inicio de sesión]<img width="752" height="296" alt="image" src="https://github.com/user-attachments/assets/182dbe78-2bf9-41f5-97c7-fe12923de7f1" />


---

### Salida del Sistema del Dashboard
<img width="918" height="415" alt="image" src="https://github.com/user-attachments/assets/8791d5e1-b438-4e5a-b9e7-19c667d19ded" />

# Mi_Hotel_Booking

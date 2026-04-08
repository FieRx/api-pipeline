# API Pipeline - E-commerce Data
Pipeline que consume datos de la API de e-commerce, los transforma, y los guarda particionados.

## Setup
1. Clonar el repo
2. Crear un archivo `.env` con el token:
   ```
   API_TOKEN=mi_token
   ```
3. Instalar dependencias:
   ```bash
   pip install -r requirements.txt
   ```

## Uso
```bash
python main.py
```

## Output
Los datos se guardan en `output/` particionados por año y mes:
```
output/
├── orders/
│   ├── order_year=2024/
│   │   ├── order_month=2024-01/
│   │   ├── order_month=2024-02/
│   │   └── ...
└── orders_all.parquet
```

## Docker
Se añade Dockerfile que permite crear la imagen y correr el container usando Docker Desktop. 
## Comandos Docker
docker build -t api-pipeline .
docker run -p <PORT> api-pipeline

## Autor
Reinaldo Franco

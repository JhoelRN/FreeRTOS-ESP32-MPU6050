ESP32 FREERTOS MPU6050



### File Structure
    .
    ├── Components              # Contiene archivos de una biblioteca específica de funciones o hardware utilizado
    │    ├──I2Cdev              # Biblioteca para comunicación I2C
    │    ├──MPU6050             # Biblioteca para sensor MPU6050
    │    ├──CMakeLists.txt      # contiene comandos para incluir el componente dado en un esp-idf 
    ├── docs                    # Archivos de documentación 
    │   ├── report.pdf          # Reporte de Proyecto
    │   └── results             # Carpeta que contiene capturas de pantalla, imágenes y videos de resultados
    ├── main                    # Archivos de origen (alternativamente, `lib` o` app`)
    │   ├──main.c               # Código fuente principal a ejecutar
    │   ├──kconfig.projbuild    # define las entradas del menú de configuración
    │   ├──CMakeLists.txt       # contiene comandos para incluir la biblioteca bluetooth y main.c en esp-idf
    ├── CmakeLists.txt          # contiene comandos para incluir componentes y carpeta principal mientras se ejecuta
    ├── LICENSE
    └── README.md 
 


![image](https://user-images.githubusercontent.com/62358739/128577984-1d5778cf-cf7d-4efe-9507-e0445d4a98e9.png)





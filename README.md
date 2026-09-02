# Motor de Inferencia

## Explicación de motor de inferencia

## Justificación de desafios implementados

**Nivel 1**

Reglas añadidas a la base de conocimiento:
```python
    {
        "id": "R08",
        "descripcion": "Falla de batería del sistema (Bios)",
        "condiciones": ["enciende", "hora_desconfigurada", "zona_horaria"],
        "conclusion": "Remplazar la batería de la tarjeta madre",
        "confianza": 0.95
    },
    {
        "id": "R09",
        "descripcion": "Problemas de red o interfaz Wi-Fi",
        "condiciones": ["enciende", "sin_conexion_internet", "icono_red_deshabilitado"],
        "conclusion": "Reinstalar controlador de red o reemplazar tarjeta Wi-Fi/Ethernet",
        "confianza": 0.85
    },
    {
        "id": "R10",
        "descripcion": "Archivos del sistema operativo corruptos",
        "condiciones": ["enciende", "pantalla_azul_frecuente", "error_archivos_sistema"],
        "conclusion": "Ejecutar recuperación de sistema operativo o ejecutarsfc /scannow y DISM desde la consola de comandos como administrador",
        "confianza": 0.91
    },
```

Se añaden las reglas siguiendo la sintaxis de los sintomas originales, adicional se incluyen las preguntas adicionales para completar el cumplimiento de las reglas mostradas.

Preguntas añadidas:
```python
    "hora_desconfigurada":      "¿La fecha y hora se desconfiguran al apagar el equipo?",
    "zona_horaria":             "¿La zona horaria está configurada correctamente?",
    "sin_conexion_internet":    "¿El equipo no detecta redes ni permite conectarse a internet?",
    "icono_red_deshabilitado":  "¿El icono de red aparece con una 'X' roja o desactivado?",
    "error_archivos_sistema":   "¿Aparecen mensajes de error indicando que faltan archivos del sistema?",
```

En base a las reglas añadidas se realizan las pruebas manuales para evaluar el correcto funcionamiento de las mismas

![Prueba reglas](./media/image.png)
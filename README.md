# Fuente de Alimentación Ajustable LM317

![Estado](https://img.shields.io/badge/Estado-Completado-success)
![Tipo](https://img.shields.io/badge/Tipo-Electrónica%20Analógica-blue)
![PCB](https://img.shields.io/badge/PCB-1%20Capa-green)
![Licencia](https://img.shields.io/badge/Licencia-MIT-blue)

Fuente de alimentación DC ajustable basada en el regulador lineal LM317. El proyecto incluye diseño esquemático, layout de PCB y validación práctica de una fuente regulada para laboratorio de electrónica y prototipado.

---

## Descripción del Proyecto

Este proyecto consiste en el diseño e implementación de una fuente de alimentación lineal ajustable utilizando el regulador de voltaje LM317. El sistema convierte el voltaje AC proveniente del secundario de un transformador en una salida DC estable y regulada, adecuada para alimentar circuitos electrónicos.

El diseño sigue una arquitectura clásica de fuentes lineales:

1. **Rectificación** de la señal AC mediante un puente de diodos
2. **Filtrado** para reducir el rizado (ripple)
3. **Regulación** de voltaje usando el LM317

La PCB fue diseñada para ser fabricada manualmente mediante técnicas de grabado químico en placa de cobre, utilizando componentes through-hole que facilitan el ensamblaje y depuración del circuito.

Este proyecto demuestra conceptos fundamentales de electrónica analógica:

- Conversión AC/DC
- Filtrado de ripple
- Regulación lineal de voltaje
- Selección de componentes
- Diseño de PCB de potencia
- Comportamiento bajo carga

---

## Características

- Voltaje de salida DC ajustable
- Regulación lineal de bajo ruido
- Rectificador de onda completa
- Filtro capacitivo de alto valor
- Referencia interna de 1.25V del LM317
- LED indicador de salida
- Componentes through-hole fáciles de soldar
- PCB de una sola capa
- Diseño compacto y funcional
- Apto para fabricación casera

---

## Especificaciones Técnicas

| Parámetro | Valor |
|----------|------|
| Regulador | LM317 |
| Entrada | AC desde transformador |
| Transformador recomendado | 18 VAC |
| Rectificación | Puente de diodos (1N4007) |
| Capacitor de filtro | 4700 µF |
| Voltaje de salida | Ajustable |
| Tipo de regulación | Lineal |
| PCB | Una capa |
| Montaje | Through-hole |
| Indicador | LED |

---

## Funcionamiento

El circuito se divide en tres etapas principales:

### 1. Rectificación

Un puente de 4 diodos convierte la señal AC del transformador en una señal DC pulsante.

### 2. Filtrado

Un capacitor electrolítico de alta capacidad reduce el rizado almacenando energía entre los ciclos de la señal rectificada.

### 3. Regulación

El LM317 mantiene un voltaje estable en la salida mediante una red de resistencias que determina el valor final del voltaje.

La ecuación que define el voltaje de salida es:
Vout = 1.25 + (1 + R2/R1)


Valores típicos:

- R1 = 240 Ω
- R2 = Potenciómetro 10k
- 1.25V = referencia interna del LM317

El potenciómetro permite ajustar el voltaje según los requerimientos del circuito conectado.

---

## Componentes

| Componente | Cantidad | Descripción |
|------------|----------|-------------|
| LM317 | 1 | Regulador de voltaje ajustable |
| 1N4007 | 4 | Diodos para puente rectificador |
| Capacitor 4700 µF | 1 | Filtrado de ripple |
| Capacitores 10 µF / 100 nF | varios | Estabilidad del regulador |
| Resistencias | varias | Divisor de voltaje y LED |
| Potenciómetro 10k | 1 | Ajuste de voltaje |
| LED | 1 | Indicador de salida |
| Borneras | 2 | Conexión AC y salida DC |

---

## Diseño del PCB

El PCB fue diseñado considerando:

- pistas cortas en rutas de potencia
- separación clara entre sección AC y DC
- pistas anchas para mayor corriente
- distribución compacta de componentes
- facilidad de fabricación manual
- accesibilidad para soldadura
- reducción de ruido eléctrico

Todos los componentes son through-hole para facilitar el montaje en entornos educativos.

---

## Aplicaciones

- Fuente de laboratorio para electrónica
- Pruebas de circuitos analógicos
- Alimentación de módulos digitales
- Prototipado de proyectos electrónicos
- Prácticas académicas
- Aprendizaje de regulación lineal

---

## Troubleshooting

### Problema: El voltaje no cambia al ajustar el potenciómetro

**Posibles causas:**

- conexión incorrecta del potenciómetro
- divisor de voltaje mal cableado
- pinout incorrecto del LM317
- soldaduras defectuosas

---

### Problema: Voltaje de salida muy bajo

**Posibles causas:**

- transformador con voltaje insuficiente
- ripple elevado por capacitor pequeño
- carga con consumo alto
- caída de voltaje en diodos

---

### Problema: El voltaje cae al conectar carga

**Posibles causas:**

- corriente insuficiente del transformador
- capacitor de filtrado insuficiente
- protección térmica del LM317
- consumo de corriente excesivo

---

### Problema: El LED no enciende

**Posibles causas:**

- polaridad invertida
- resistencia limitadora incorrecta
- ausencia de voltaje en la salida

---

### Problema: Ripple excesivo

**Posibles causas:**

- capacitor de bajo valor
- alta corriente de carga
- capacitor defectuoso
- mala conexión a tierra

---

## Mejoras Futuras

- limitador de corriente
- voltímetro digital integrado
- mayor capacidad de corriente
- mejor disipación térmica
- protección contra cortocircuito
- gabinete de protección
- filtrado adicional (<2% ripple)
- múltiples salidas
- indicador digital de corriente

---

## Autor

**Daniel Isaac Parra Baldovino**

---

## Licencia

Este proyecto está bajo la Licencia MIT.  
Ver el archivo LICENSE para más detalles.

---

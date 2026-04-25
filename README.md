 ==========================================================
# LGM-SENTINEL RISK ENGINE v4.0
# Autor: César Octavio García Martínez
# ==========================================================

import numpy as np

def teorema_cega_ivp(v, c, E, r, k):
    """
    Fórmula: IVP = (v*c + E) / sqrt(r*k)
    v: función de cambio/vector, c: constante, E: Entropía/Emoción
    r: Resistencia, k: Rigidez
    """
    ivp = (v * c + E) / np.sqrt(r * k)
    return ivp

# Verificación de Salto de Heaviside
def alerta_heaviside(actual, previo, umbral=1.5):
    if abs(actual - previo) > umbral:
        return "ALERTA CRÍTICA: SALIDA TOTAL DEL MERCADO"
    return "ESTADO: ESTABLE"

print("Motor LGM v4.0 cargado satisfactoriamente.")

# 1. Calculamos los hallazgos clave
fuga_total = df['Churn'].value_counts(normalize=True)['Yes'] * 100
fuga_mes_a_mes = df[df['Contract'] == 'Month-to-month']['Churn'].value_counts(normalize=True)['Yes'] * 100
fuga_sin_soporte = df[df['TechSupport'] == 'No']['Churn'].value_counts(normalize=True)['Yes'] * 100

# 2. Imprimimos el Resumen Ejecutivo
print("-" * 50)
print("📝 RESUMEN EJECUTIVO PARA EL PORTAFOLIO")
print("-" * 50)
print(f"📊 Tasa General de Fuga: {fuga_total:.2f}%")
print(f"🚩 Alerta Roja: Los clientes con contrato 'Mes a Mes' se fugan un {fuga_mes_a_mes:.2f}%.")
print(f"🛠️ Oportunidad: Los clientes sin Soporte Técnico tienen una fuga del {fuga_sin_soporte:.2f}%.")
print("-" * 50)

# 3. Una última visualización de impacto: Distribución de antigüedad
plt.figure(figsize=(10, 5))
sns.histplot(data=df, x='tenure', hue='Churn', kde=True, element="step", palette='crest')
plt.title('Distribución de la Antigüedad de los Clientes (Tenure)')
plt.xlabel('Meses en la Compañía')
plt.ylabel('Cantidad de Clientes')
plt.show()
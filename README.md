# cristian-castro
# Matriz de inventario
# [Código, Nombre, Stock Actual, Stock Mínimo]

inventario = [
    [101, "Teclado", 3, 10],
    [102, "Mouse", 15, 10],
    [103, "Monitor", 2, 5],
    [104, "Audifonos", 8, 8],
    [105, "Memoria USB", 1, 6]
]

# Función para calcular la cantidad a pedir
def calcular_pedido(stock_actual, stock_minimo):

    if stock_actual < stock_minimo:
        cantidad = stock_minimo - stock_actual
    else:
        cantidad = 0

    return cantidad


# Mostrar resultados
print("===== LISTA DE PEDIDOS =====")

for articulo in inventario:

    codigo = articulo[0]
    nombre = articulo[1]
    stock_actual = articulo[2]
    stock_minimo = articulo[3]

    pedido = calcular_pedido(stock_actual, stock_minimo)

    print("Artículo:", nombre)
    print("Código:", codigo)
    print("Cantidad a pedir:", pedido)
    print("----------------------------")

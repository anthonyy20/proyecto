# proyecto
integrantes:Julio Moran, Jordan Zambrano,Ricardo García,Johan Ortega
    Codigo
mport networkx as nx
import matplotlib.pyplot as plt

class SimuladorRed:
    def _init_(self):

        self.grafo = nx.Graph()

    def agregar_enlace(self, nodo1, nodo2):
        self.grafo.add_edge(nodo1, nodo2)

    def visualizar_red(self, color='blue'):

        nx.draw(self.grafo, with_labels=True, font_weight='bold', node_color=color)
        plt.show()
import networkx as nx
import matplotlib.pyplot as plt

class SimuladorRed:
    def _init_(self):
        # Crear la grafica de red utilizando la biblioteca NetworkX
        self.grafo = nx.Graph()

    def agregar_enlace(self, nodo1, nodo2):
        self.grafo.add_edge(nodo1, nodo2)

    def visualizar_red(self, color='blue'):
        # Visualizar la grafica por medio de Matplotlib
        nx.draw(self.grafo, with_labels=True, font_weight='bold', node_color=color)
        plt.show()

    def desconectar_enlace(self, nodo1, nodo2):
        # Verificación
        if self.grafo.has_edge(nodo1, nodo2):
            print(f"Desconectando enlace entre {nodo1} y {nodo2}")
            self.grafo.remove_edge(nodo1, nodo2)
        else:
            print(f"No existe enlace entre {nodo1} y {nodo2}")
if _name_ == "_main_":
    simulador = SimuladorRed()

    simulador.agregar_enlace('RouterA', 'RouterB')
    simulador.agregar_enlace('RouterB', 'RouterC')
    simulador.agregar_enlace('RouterC', 'RouterD')

    print("Red original:")
    simulador.visualizar_red(color='green')

    simulador.desconectar_enlace('RouterB', 'RouterC')

    print("\nRed después de desconectar el enlace:")
    simulador.visualizar_red(color='red')

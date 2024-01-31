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

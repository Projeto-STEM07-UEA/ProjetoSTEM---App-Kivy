# ProjetoSTEM---App-Kivy
App desenvolvido em kivy

import kivy
from kivy.app import App
from kivy.uix.floatlayout import FloatLayout
from kivy.uix.widget import Widget
from kivy.uix.screenmanager import ScreenManager, Screen
from kivy.uix.image import Image

class Manager(ScreenManager):
	pass

class Menu(Screen):
	pass 

class Game(Screen):
	pass
	
class Basico(Screen):
	pass

class Medio(Screen):
	pass

class Avancado(Screen):
	pass

class ArduQuiz(App):
	pass

if __name__ == "__main__":
	ArduQuiz().run()


#Arquivo em .kv
Manager:
	Menu:
		name:'menu'
	Game:
		name:'game'
	Basico:
		name:'basico'
	Medio:
		name:'medio'
	Avancado:
		name:'avancado'

#<MenuButton@Button>:
	#font_size:'50sp'
	#background_normal:'menuButton.png'
	#background_down:'menuButtonpressed.png'
	#border: 90,90,90,90

<Menu>:
	BoxLayout:
		canvas:
			Color:
				rgba:1,1,1,1
			Rectangle:
				size:self.size
				pos:self.pos
				

		orientation: 'vertical'
		padding: '200dp', '50dp'
		spacing:'100dp'
		Widget:
		BoxLayout:
			padding:"100dp"
			spacing:"150dp"
			Button:
				text:'Start'
				on_press:
				on_release:app.root.current = 'game'
			Button:
				text:'Exit'
				on_press:
				on_release:app.Stop()



<Game>:
	FloatLayout:
		canvas:
			Color:
				rgba:1,0.9,1,1
			Rectangle:
				size:self.size
				pos:self.pos
		orientation: 'horizontal'
		padding: '200dp', '50dp'
		spacing:'100dp'
		Widget:
		BoxLayout:
			padding:"100dp"
			spacing:"150dp"
			Button:
				text:'Básico'
				on_press:
				on_release:app.root.current = 'basico'
			Button:
				text:'Médio'
				on_press:
				on_release:app.root.current = 'medio'
			Button:
				text:'AvanÇado'
				on_press:
				on_release:app.root.current = 'avancado'


<Basico>:
	FloatLayout:
		canvas:
			Color:
				rgba:1,1,1,1
			Rectangle:
				size:self.size
				pos:self.pos
		orientation:'vertical'
		padding: '200dp', '50dp'
		spacing:'100dp'


<Medio>:
	FloatLayout:
		canvas:
			Color:
				rgba:1,1,1,1
			Rectangle:
				size:self.size
				pos:self.pos
		orientation:'vertical'
		padding: '200dp', '50dp'
		spacing:'100dp'


<Avancado>:
	FloatLayout:
		canvas:
			Color:
				rgba:1,1,1,1
			Rectangle:
				size:self.size
				pos:self.pos
		orientation:'vertical'
		padding: '200dp', '50dp'
		spacing:'100dp'


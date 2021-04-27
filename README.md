# ProjetoSTEM---App-Kivy
App desenvolvido em kivy

import kivy
from kivy.app import App
from kivy.uix.floatlayout import FloatLayout
from kivy.uix.widget import Widget
from kivy.uix.screenmanager import ScreenManager, Screen
from kivy.uix.image import Image
from kivy.properties import ObjectProperty

class Manager(ScreenManager):
	pass

class Menu(Screen):
	pass 

class Game(Screen):
	pass
	
class Comandos(Screen):
	pass

class Hardware(Screen):
	pass

class Experimentos(Screen):
	pass
	
class ArduApp(App):
	pass

if __name__ == "__main__":
	ArduApp().run()


#Arquivo em .kv
Manager:
	Menu:
		name:'menu'
	Game:
		name:'game'
	Comandos:
		name:'comandos'
	Hardware:
		name:'medio'
	Experimentos:
		name:'experimentos'
	
<MenuButton@Button>:
	font_size:'50sp'
	background_normal:'menuButton.png'
	background_down:'menuButtonpressed.png'
	border: 90,90,90,90

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
			MenuButton:
				text:'Start'
				on_press:
				on_release:app.root.current = 'game'
			MenuButton:
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
		orientation: 'vertical'
		padding: '200dp', '50dp'
		spacing:'100dp'
		Widget:
		BoxLayout:
			orientation: "vertical"
			padding:"600dp", "50dp"
			spacing:"100dp"
			Button:
				text:'Voltar'
				on_release:app.root.current = 'menu'
			Button:
				text:'Comandos'
				on_press:
				on_release:app.root.current = 'comandos'
			Button:
				text:'Hardware'
				on_press:
				on_release:app.root.current = 'hardware'
			Button:
				text:'Experimentos'
				on_press:
				on_release:app.root.current = 'experimentos'


<Comandos>:
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
		BoxLayout:
			orientation: "vertical"
			padding:"600dp", "50dp"
			spacing:"100dp"
			Button:
				text:'Voltar'
				on_release:app.root.current = 'game'

<Hardware>:
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


<Experimentos>:
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



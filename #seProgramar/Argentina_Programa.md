# Argentina Programa

## Gobstones
### Ejercicio 1
´´´
procedure DibujarLadoEscalera() {
    repeat(4){ # N lugar -1
        Poner(Negro)
        Mover(Norte)
    }
    Poner(Negro)
}

program {
    DibujarLadoEscalera()
    Mover(Este)
    Mover(Sur)
    Poner(Negro)
    repeat(2){ Mover(Sur) }
    Poner(Negro)
    Mover(Sur)
    Mover(Este)
    DibujarLadoEscalera()
}
´´´

### Ejercicio 2
´´´

procedure DibujarMesa(color) {
    repeat(2){ 
        Poner(color)
        Mover(Norte)
    }
    repeat(3){ 
        Poner(color)
        Mover(Este)    
        }
    repeat(2){ 
        Poner(color)
        Mover(Sur)
        }
    Poner(color)
}

´´´
## JAVASCRIPT
### Ejercicio 3
´´´
function concatenacionEsIgual(a, b, c) {
    return ( a + b === c ) 
}
´´´

### Ejercicio 4
function saludar (nombre, hora) {
    let out;
    if (hora < 12) {
        out = 'Buenos dias ' + nombre
    }else {
        out = 'Buenas tardes ' + nombre
    }
    return out
}

### Ejercicio 5
function sumaDeLosMayoresASiete(valores) {
    let suma = 0;
    valores.forEach(valor => {
        if(valor>7){
            suma = suma + valor;
        }
    });
    return suma
}
### Ejercicio 6
function resumenCancion(cancion){
    return (
        cancion.nombre 
        + ' de la banda ' 
        + cancion.banda 
        + ' tiene una duracion de ' 
        + cancion.duracion * 60 
        + ' segundos'  
    )
} 

## Ruby 
### Ejercicio 7
module AguaParaMate
    @temperatura = 0
    def self.temperatura
        @temperatura
    end

    def self.calentar_agua!(grados)
        @temperatura += grados
    end

    def self.temperatura_exacta?
        @temperatura == 80
    end
end

### Ejercicio 8 
#  MAP USO
module Biblioteca
    @libros = [Fundacion, Contacto, LaInsoportableLevedadDelSer, Socorro, ComoAguaParaChocolate]
    def self.nombres_de_libros 
        @libros.map {|libro| libro.nombre}
    end
end

### Ejercicio 9
#Clases
´´´
class Camion
  def initialize(muebles)
    @muebles = muebles
  end
  def cargar_muebles!
    @muebles.each{ |mueble| mueble.ser_cargado!}
  end  
end

class Colchon
  def initialize(resortes)
    @cantidad_de_resortes = resortes
  end
  def ser_cargado!
    @cantidad_de_resortes -= 4
  end
  def cantidad_de_resortes
    @cantidad_de_resortes
  end
end

class Sillon
  def initialize(polvo)
    @nivel_de_polvo = polvo
  end
  def self.ser_cargado!
    @nivel_de_polvo += 20
  end
  def nivel_de_polvo
    @nivel_de_polvo
  end
end

class Electrodomestico
  def ser_cargado!
  
  end
end
´´´

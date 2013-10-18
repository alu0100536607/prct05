# Implementar en este fichero la clase para crear objetos racionales

require "./gcd.rb"

class Fraccion
	def initialize(u,v)
	@numerador = u
	@denominador = v
	end
	def mcd(a,b)
  		while b != 0
    			a, b = b,a % b
  		end
  		a
	end
	def mcm(a,b)	
		(a/mcd(a,b))*b
	end
	def to_s
		puts "#{@numerador}/#{@denominador}"
	end
	def suma(a,b)
		denominador = mcm(@denominador,b)
		numerador = ((denominador/@denominador) * @numerador ) + ((denominador/b) * a)
		puts "#{numerador}/#{denominador}"
	end
	def resta(a,b)
		denominador = mcm(@denominador,b)
		numerador = ((denominador/@denominador) * @numerador ) - ((denominador/b) * a)
		puts "#{numerador}/#{denominador}"	
	end
	def producto(a,b)
		numerador = @numerador * a
		denominador = @denominador * b
		puts "#{numerador}/#{denominador}"
	end
	def division(a,b)	
		numerador = @numerador*b
		denominador = @denominador*a
		puts "#{numerador}/#{denominador}"
	end

end

ejemplo = Fraccion.new(10,5)
ejemplo.to_s
ejemplo.suma(3,2)
ejemplo.resta(3,2)
ejemplo.producto(3,2)
ejemplo.division(3,2)


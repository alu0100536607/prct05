¿Cuál es el error en el código del método para calcular el máximo común divisor?

	No se puede usar (v == 0) como condición del while, ya que así no entra nunca. Tiene que ser (v != 0)

¿Qué comandos del depurador utilizó para detectarlo? Describa la sesión de depuración.

	l y s

	gcd.rb:1:def gcd(u, v)
	(rdb:1) l
	[-4, 5] in gcd.rb
	=> 1  def gcd(u, v)
   	2    u, v = u.abs, v.abs
   	3    while v == 0
   	4      u, v = v, u % v
   	5    end
	(rdb:1) s
	gcd.rb:9:puts gcd(5,10)
	(rdb:1) s
	gcd.rb:2:  u, v = u.abs, v.abs
	(rdb:1) s
	gcd.rb:3:  while v == 0  <= Aquí podemos ver como no entra en el while
	(rdb:1) s
	gcd.rb:6:  u
	(rdb:1) s
	5


<?php	
	//validamos que se haya enviado el formulario 
	if(isset($_POST['operacion']))
		{	
    //recogemos nuestros valores 
	//variable uno pnumero
	$var1 = $_POST['pnumero'];
	$var2 = $_POST['snumero'];
		
		if($var1 > 10)
			{
		//realizamos la operacion 
		$suma 	= $var1 + $var2;
		$resta 	= $var1 - $var2;
		$multi 	= $var1 * $var2;
		$divi 	= $var1 / $var2;
		//imprimimos el resultado 
		print $suma; 
		echo '<br>';
		print $resta; 
		echo '<br>';
		print $multi; 
		echo '<br>';
		print $divi; 
		echo '<br>';
			}
		else
			{
			echo "El primer numero no cumple con los parametros necesarios";
			}
		
		}
	else
		{
?>	
	<form action="archivo.php" method="post">
	<label>Ingrese el primer numero</label><br>
		<input type="text" name='pnumero'><br>
		<label>Ingrese el segundo numero</label><br>
		<input type="text" name="snumero">
		<br>
		<input type="submit" name="operacion" value="Sumar">
	</form>
	
<?php		
		}
?>

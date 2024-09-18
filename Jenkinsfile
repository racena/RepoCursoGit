def fechaNacimiento = 1982
def fechaHoy = 2024
def edad

pipeline
{
    agent any
	
    stages
    {
 
		stage("CalcularEdad")
        {
            steps
            {
                script
                {
					edad = fechaHoy - fechaNacimiento
                    println("La edad es:"+edad)
					
					//Escribe a fichero
					nombreFichero="C:\\Fichero_Salida.txt"
                    writeFile(file:nombreFichero , text:edad)
                    println("El fichero fue escrito. Vamos a leerlo:")
					
					//Lee el fichero
					txt = readFile(file:nombreFichero)
                    println (txt)
				}
            }
        }
		
        stage("GenerarTxt")
        {
            steps
            {
                script
                {
					//Escribe a fichero
					nombreFichero="C:\\edad.txt"
                    writeFile(file:nombreFichero, edad)
                    println("El fichero fue escrito. Vamos a leerlo:")
					
					//Lee el fichero
					txt = readFile(file:nombreFichero)
                    println (txt)
                }
            }
        }
    }

}

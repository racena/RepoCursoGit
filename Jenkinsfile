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
					nombreFichero="C:\\Fichero_Salida.txt"
                    writeFile(file:nombreFichero , text:"La edad es "+edad)
                    println("El fichero fue escrito. Vamos a leerlo:")
					
					//Lee el fichero
					txt = readFile(file:nombreFichero)
                    println (txt)
                }
            }
        }
    }

}

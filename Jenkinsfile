def fechaNacimiento = new Date('08/21/1982')
def fechaHoy = new Date()
def edad = 0

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
					edad = fechaHoy.getYear() - fechaNacimiento.getYear()
                    println("La edad es:"+edad)
					
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

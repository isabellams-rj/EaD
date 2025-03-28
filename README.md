# EaD
Sor só consigo mandar a 9 e a 10, as outras ficaram no computador do curso
questao 9

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exibir Data e Hora Atual</title>
</head>
<body>

    <h2>Exibir Data e Hora Atual</h2>
    
    <button id="mostrarDataHora">Mostrar Data e Hora</button>
    
    <p id="dataHoraAtual"></p>

    <script>
        document.getElementById('mostrarDataHora').addEventListener('click', function() {
          
            var dataHora = new Date();
            
          
            var dataFormatada = dataHora.toLocaleString('pt-BR', {
                weekday: 'long', 
                year: 'numeric', 
                month: 'long', 
                day: 'numeric',
                hour: 'numeric',
                minute: 'numeric',
                second: 'numeric',
                hour12: true
            });
            
           
            document.getElementById('dataHoraAtual').innerText = 'Data e Hora Atual: ' + dataFormatada;
        });
    </script>

</body>
</html>

questao 10 
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simulação de Carregamento</title>
    
</head>
<body>

    <h2>Simulação de Carregamento</h2>
    
    <button id="iniciarCarregamento">Iniciar Carregamento</button>
    
    <div class="barra-container">
        <div id="barraProgresso" class="barra-progresso">0%</div>
    </div>
    
    <p id="status" class="status"></p>

    <script>
        document.getElementById('iniciarCarregamento').addEventListener('click', function() {
            var barra = document.getElementById('barraProgresso');
            var status = document.getElementById('status');
            var progresso = 0;

            
            var intervalo = setInterval(function() {
                progresso += 1;  
                barra.style.width = progresso + '%'; 
                barra.innerText = progresso + '%';  

               
                status.innerText = 'Carregando... ' + progresso + '%';

                if (progresso >= 100) {
                    clearInterval(intervalo); 
                    status.innerText = 'Carregamento Concluído!';
                }
            }, 100); 
        });
    </script>

</body>
</html>

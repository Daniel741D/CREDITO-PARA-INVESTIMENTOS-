<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Solicite Análise de Crédito</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; padding: 20px; }
        .container { max-width: 600px; margin: auto; }
        h1 { color: #007bff; }
        .form-container { background: #f8f9fa; padding: 20px; border-radius: 8px; }
        input, select, button { width: 100%; padding: 10px; margin: 5px 0; }
        button { background: #007bff; color: white; border: none; cursor: pointer; }
        
        /* Estilos para o destaque da área de investimento */
        label[for="area"] {
            font-size: 1.2em;
            color: #007bff;
            font-weight: bold;
            margin-top: 20px;
            display: block;
        }

        select#area {
            background-color: #e9ecef;
            border: 2px solid #007bff;
            font-size: 1.1em;
            padding: 12px;
            border-radius: 8px;
        }

        h2 {
            margin-top: 20px;
            color: #343a40;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Solicite Sua Análise de Crédito para Investimento</h1>
        <p>Preencha o formulário abaixo e entraremos em contato pelo WhatsApp.</p>
        
        <div class="form-container">
            <h2>Preencha seus dados:</h2>
            <form action="https://wa.me/SEUNUMEROWHATSAPP" method="get" target="_blank" id="whatsappForm">
                <input type="text" name="nome" id="nome" placeholder="Seu Nome" required>
                <input type="email" name="email" id="email" placeholder="Seu E-mail" required>
                <input type="tel" name="telefone" id="telefone" placeholder="Seu Telefone" required>
                
                <label for="area">Área de Investimento:</label>
                <select name="area" id="area" required>
                    <option value="">Selecione a Área de Investimento</option>
                    <option value="Área Rural">Área Rural</option>
                    <option value="Veículo">Veículo</option>
                    <option value="Imóvel">Imóvel</option>
                    <option value="Construção">Construção</option>
                    <option value="Reforma">Reforma</option>
                    <option value="Loja/Ponto Comercial">Loja/Ponto Comercial</option>
                </select>

                <select name="valor" id="valor" required>
                    <option value="">Selecione o Valor Desejado</option>
                    <option value="100000">R$ 100.000</option>
                    <option value="200000">R$ 200.000</option>
                    <option value="300000">R$ 300.000</option>
                    <option value="400000">R$ 400.000</option>
                    <option value="500000">R$ 500.000</option>
                    <option value="600000">R$ 600.000</option>
                    <option value="700000">R$ 700.000</option>
                    <option value="800000">R$ 800.000</option>
                    <option value="900000">R$ 900.000</option>
                    <option value="1000000">R$ 1.000.000</option>
                </select>
                
                <button type="submit">Enviar para WhatsApp</button>
            </form>
        </div>
    </div>

    <script>
        // Quando o formulário for enviado, cria o link para o WhatsApp
        document.getElementById("whatsappForm").onsubmit = function(event) {
            event.preventDefault(); // Evita o envio do formulário

            var nome = document.getElementById("nome").value;
            var email = document.getElementById("email").value;
            var telefone = document.getElementById("telefone").value;
            var area = document.getElementById("area").value;
            var valor = document.getElementById("valor").value;

            // Mensagem que será enviada
            var mensagem = encodeURIComponent(`Tenho interesse em Crédito para Investimento\n\n*Solicitação de Crédito para Investimento*\n\nNome: ${nome}\nE-mail: ${email}\nTelefone: ${telefone}\nÁrea de Investimento: ${area}\nValor Desejado: R$ ${valor}`);

            var url = `https://wa.me/5598984699652?text=${mensagem}`;

            window.open(url, '_blank'); // Abre o link do WhatsApp
        };
    </script>
</body>
</html>

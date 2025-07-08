// Função para converter Celsius para Fahrenheit
function celsiusParaFahrenheit(celsius) {
    return (celsius * 9/5) + 32;
}

// Função para converter Celsius para Kelvin
function celsiusParaKelvin(celsius) {
    return celsius + 273.15;
}

// Função principal
function converterTemperatura() {
    // Solicita ao usuário a temperatura em Celsius
    let celsius = parseFloat(prompt("Digite a temperatura em Celsius (°C):"));

    // Verifica se a entrada é um número válido
    if (isNaN(celsius)) {
        alert("Por favor, digite um número válido.");
        return;
    }

    // Realiza as conversões
    let fahrenheit = celsiusParaFahrenheit(celsius);
    let kelvin = celsiusParaKelvin(celsius);

    // Exibe os resultados
    alert(
        `Temperatura em Celsius: ${celsius.toFixed(2)} °C\n` +
        `Temperatura em Fahrenheit: ${fahrenheit.toFixed(2)} °F\n` +
        `Temperatura em Kelvin: ${kelvin.toFixed(2)} K`
    );
}

// Executa a função
converterTemperatura();

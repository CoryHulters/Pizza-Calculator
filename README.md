<html>
    <body>

        <h1> Pizza Calculator </h1>

<!--Applicatie Ontwikkeling
Cory Hulters-->
        <!--Maakt elke input en prijs label voor elke maat pizza-->
        Small Pizzas: <input type="text" id = "SmallPizza" name="Small Pizzas" value="0"><br> <p>Cost: &euro; 1.00</p>
        Medium Pizzas: <input type="text" id = "MediumPizza" name="Medium Pizzas" value="0"><br> <p>Cost: &euro; 2.00</p>
        Large Pizzas: <input type="text" id = "LargePizza" name="Large Pizzas" value="0"><br> <p>Cost: &euro; 3.00</p>

        <button id="PriceCalc" type="submit" name="action">Checkout</button>

         <p id = "Total" ></p> <!--Laat eerst de prijs zien zonder tekst totdat de bestelling is verzonden-->

         
        <script type="text/javascript">

        const SmallPizzaPrice = 1;
        const MediumPizzaPrice = 2;
        const LargePizzaPrice = 3;

        var Price;

        var Calculate = document.getElementById('PriceCalc');
        var SmallPizzas = document.getElementById('SmallPizza');
        var MediumPizzas = document.getElementById('MediumPizza');
        var LargePizzas = document.getElementById('LargePizza');

        //Als je op deze knop klikt wordt de totale prijs van de bestelling berekend
        Calculate.onclick = function() {
          Price = (SmallPizzas.value * SmallPizzaPrice) + (MediumPizzas.value * MediumPizzaPrice) + (LargePizzas.value * LargePizzaPrice); //Formule
          Total.innerHTML = "Your total is going to be &euro;" + Price + "."; //Laat de totale prijs zien van jouw bestelling
        }

        </script>
    </body>
</html>

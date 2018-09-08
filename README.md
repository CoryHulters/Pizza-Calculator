<html>
    <body>

        <h1> Pizza Calculator </h1>

        <!--Maakt elke input en prijs label voor elke maat pizza-->
        Small Pizzas: <input type="text" id = "SmallPizza" name="Small Pizzas" value="0"><br> <p>Cost: €1.00</p>
        Medium Pizzas: <input type="text" id = "MediumPizza" name="Medium Pizzas" value="0"><br> <p>Cost: €2.00</p>
        Large Pizzas: <input type="text" id = "LargePizza" name="Large Pizzas" value="0"><br> <p>Cost: €3.00</p>

        <button id="PriceCalc" type="submit" name="action">Checkout</button>

         <p id = "Total" ></p> <!--Laat eerst de prijs zien zonder tekst totdat de bestelling is verzonden-->

         
        <script type="text/javascript">

        const SmallPizzaPrice = 1;
        const MediumPizzaPrice = 2;
        const LargePizzaPrice = 3;

        var Price;

        let Calculate = document.getElementById('PriceCalc');
        let SmallPizzas = document.getElementById('SmallPizza');
        let MediumPizzas = document.getElementById('MediumPizza');
        let LargePizzas = document.getElementById('LargePizza');

        //Als je op deze knop klikt wordt de totale prijs van de bestelling berekend
        Calculate.onclick = function() {
          Price = (SmallPizzas.value * SmallPizzaPrice) + (MediumPizzas.value * MediumPizzaPrice) + (LargePizzas.value * LargePizzaPrice); //Formule
          Total.innerHTML = "Your total is going to be €" + Price + "."; //Laat de totale prijs zien van jouw bestelling
        }

        </script>
    </body>
</html>

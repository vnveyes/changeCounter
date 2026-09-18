<script lang="ts">

    let counter =  $state(0);

    function addNum(num: number){
        counter = Math.round(( counter + num ) * 100) / 100;
    }
        
    function resetNum() {
        counter = 0;
    }

</script>

<div class="app">
    <div class="card">
        <h1>Change Counter</h1>
        
        <h2 class="counter">${counter.toFixed(2)}</h2>
        <button class="Box" onclick={() => addNum(0.01)}>$0.01</button>
        <button class="Box" onclick={() => addNum(0.05)}>$0.05</button>
        <button class="Box" onclick={() => addNum(0.10)}>$0.10</button>
        <button class="Box" onclick={() => addNum(0.25)}>$0.25</button>
        <button class="Box" onclick={() => addNum(0.50)}>$0.50</button>
        <button class="Box" onclick={() => addNum(1.00)}>$1.00</button>
		<button class="ResetBox" onclick={() => resetNum()}>Reset</button>
</div>
</div>

<style>
   :global(body) {
       display: flex;
       justify-content: center;
       padding-top: 80px;
       font-family: 'Courier', monospace;
       background: linear-gradient(gold, green);
       text-align: center;
       min-height: 100vh;
       /*font-family: 'Iosevka Charon Mono', monospace;*/
   }

   .counter{
        type: "text";
        background-color: white;
        border-radius: 8px;
        height:80px;
        font-size:60px;
   }

   .Box {
       background-color: #023b0e;
       border: none;
       border-radius: 15px;
       color: rgb(143, 167, 12);
       padding: 12px 20px;
       margin: 5px;
       gap:20px;
       font-size: 20px;
       font-weight: 200;
       transition: all 0.2s;
       font-family: 'Courier', monospace;
       cursor: pointer;
       text-align: center;
   }
   
    .ResetBox {
       background-color: #023b0e;
       border: none;
       border-radius: 15px;
       color: rgb(143, 167, 12);
       padding: 12px 80px;
       margin: 5px;
       gap:20px;
       font-size: 20px;
       font-weight: 200;
       transition: all 0.2s;
       font-family: 'Courier', monospace;
       cursor: pointer;
       text-align: center;
   }

   .Box:hover {
       background-color: #adab0ce1;
       color: rgb(16, 73, 28);
   }

   .Box:active {
       background-color: #d6c80ce1;
       color: rgb(19, 172, 64);
   }

   .card {
       border-radius: 8px;
       padding: 24px;
       box-shadow: 9px 15px 9px  rgba(9, 9, 0, 9);
       width: 300px;
       background: linear-gradient(
        135deg,
        #2fdf55,
        #0a3300
       );    
   }
</style>
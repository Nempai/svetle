<main> 
  <!--  <h1>My to-do list</h1> 
    <form on:submit|preventDefault={add}> 
        <input bind:value={newItem} placeholder="Enter to-do" /> 
        <button class="add-todo" on:click={add}><span class="plus">+</span></button> 
    </form> 
    <div class="todos"> 
        {#each todoList as item, index} 
            <div class="todo" class:completed={item.completed}> 
                <span class="todo__text">{item.task}</span> 
                <div class="todo__buttons"> 
                    <button class="complete" on:click={() => complete(index)}> 
                        <Icon name="check-mark" /> 
                    </button> 
                    <button class="delete" on:click={() => remove(index)}> 
                        <Icon name="delete" /> 
                    </button> 
                </div> 
            </div> 
        {/each} 
    </div> -->


    <div class="container">
      <h1>Учет расходов</h1>
      <form on:submit|preventDefault={addExpense}>
        <input type="text" bind:value={description} placeholder="Описание">
        <input type="number" bind:value={amount} placeholder="Сумма">
        <button type="submit">Добавить</button>
      </form>
      <table>
        <thead>
          <tr>
            <th>Описание</th>
            <th>Сумма</th>
            <th>Действия</th>
          </tr>
        </thead>
        <tbody>
          {#each expenses as expense}
            <tr>
              <td>{expense.description}</td>
              <td>{expense.amount}</td>
              <td><button on:click={() => deleteExpense(expense)}>Удалить</button></td>
            </tr>
          {/each}
        </tbody>
      </table>
    </div>
</main>
<style>
    main {
  display: flex;
  flex-direction: column;
  align-items: center;
  min-height: 100%;
  padding: 5vmin;
  box-sizing: border-box;

}
table {
   border: 1px solid grey;
}
/* границы ячеек первого ряда таблицы */
th {
   border: 1px solid grey;
}
/* границы ячеек тела таблицы */
td {
   border: 1px solid grey;
}

.container {
  max-width: 600px;
  margin: 0 auto;
}

table {
  border-collapse: collapse;
  margin-top: 20px;
  width: 100%;
}

th,
td {
  padding: 10px;
  text-align: left;
}

tr:nth-child(even) {
  background-color: #f2f2f2;
}

input[type="text"],
input[type="number"],
button[type="submit"] {
  display: block;
  margin-bottom: 10px;
  padding: 10px;
  width: 100%;
  box-sizing: border-box;
}

button {
  background-color: #4CAF50;
  border: none;
  color: white;
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin-top: 10px;
  cursor: pointer;
}

button:hover {
  opacity: 0.8;
}

input:focus,
button:focus {
  outline: none;
  box-shadow: 0 0 5px #4CAF50;
}
</style>



<script> 
    let expenses = [
    { id: 1, description: "Кофе", amount: 100 }, //добавил для примера
    { id: 2, description: "Обед", amount: 300 },
    { id: 3, description: "Такси", amount: 150 }
  ]

  let description = ""
  let amount = ""

  function addExpense() {
    const newExpense = {
      id: expenses.length + 1,
      description,
      amount
    }
    expenses = [...expenses, newExpense]
    description = ""
    amount = 0
  }
  
  function deleteExpense(expense) {
    expenses = expenses.filter(e => e.id !== expense.id)
  }
</script> 
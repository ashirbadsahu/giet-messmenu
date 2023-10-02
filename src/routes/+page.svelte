<script>
    import { menus } from "$lib/index";
    let selectedDay = null; // State variable to store the selected day

    // Function to update the selected day when a button is clicked
    function selectDay(day) {
        selectedDay = day;
    }
</script>
<div class="flex items-center justify-center my-4 text-white flex-col">
    <h1 class="text-xl lg:text-2xl">GIET Menu for Central Mess</h1>
    <p class="py-2 text-lg lg:text:xl">Month: October</p>
</div>
<div class="flex items-center justify-center my-4">
    <div class="flex items-center justify-center my-4 ">
        {#each menus as menu}
        <button
            class="bg-transparent outline-none text-sm lg:text-lg border border-white-100 px-2 py-1 text-white uppercase hover:bg-white hover:text-black"
            on:click={() => selectDay(menu.day)}>
            {menu.day}
        </button>
        {/each}
    </div>
</div>

<div class="flex items-center justify-center my-10 lg:text-lg">
    {#if selectedDay !== null}
    <div class="w-64 h-68 lg:w-84 lg:h-88 rounded-lg border-2 border-white text-center">
        <div class="py-2 px-1">
        <p class="text-white py-2">Breakfast: {menus.find(menu => menu.day === selectedDay).breakfast}</p>
        <p class="text-white py-2">Lunch: {menus.find(menu => menu.day === selectedDay).lunch}</p>
        <p class="text-white py-2">Snacks: {menus.find(menu => menu.day === selectedDay).snacks}</p>
        <p class="text-white py-2">Dinner: {menus.find(menu => menu.day === selectedDay).dinner}</p>
        </div>

    </div>
    {:else}
    <p class="text-white">Select a day to view the menu.</p>
    {/if}
</div>

<div class="flex items-center justify-center my-10 text-white flex-col lg:text-lg">
    <p class="text-md">Timings</p>
    <p>Breakfast: 6:30 to 8:30 AM</p>
    <p>Lunch: 12:15 PM to 2:30 PM</p>
    <p>Tea: 6:00 PM to 7:00 PM</p>
    <p>Dinner: 8:00 PM to 9:45 PM</p><br>
    <p class="text-center justify-center text-md">Sunday and holiday</p>
    <p class="text-center justify-center">Breakfast: 8.00 AM to 9:30 AM</p>
    <p class="text-center justify-center">and Lunch: 12:30PM to 2:30 PM</p> 
</div>

<div class="bottom-0 left-0 w-full bg-transparent text-white text-center  p-2">
 <a href="https://github.com/ashirbadsahu/" target="_blank">Made with ❤️ by Ashirbad</a> 
</div>

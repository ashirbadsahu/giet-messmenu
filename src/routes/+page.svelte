<script>
    import { menus } from "$lib/index";
    
    let selectedDay = "";
    let submitted = false;
    
    function handleSubmit(event) {
        event.preventDefault();
        submitted = true;
    }

    function handleStateChange(event) {
        selectedState = event.target.value;
    }
</script>


    <div>
        <select name="" id="">
            {#each menus as menu}
               <option value={menu}>{menu.day}</option> 
            {/each}
        </select>    
    </div>
    
  


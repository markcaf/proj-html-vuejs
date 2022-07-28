<template>
  <div class="wrapper d-flex align-items-center gap-4">
    <div class="number">
        <i class="fa-solid fa-users"></i>
        <input type="number" id="book_persons" name="book_persons"
        value="1" 
        min="1" max="10">
    </div>

    <div class="text text-white text-uppercase">
        For
    </div>

    <div class="date">
        <input type="date" id="book_date" name="book_date"
        value="2020-11-29"
        min="2018-01-01" max="2018-12-31">
    </div>

    <div class="text text-white text-uppercase">
        At
    </div>

    <div class="hour">
        <input type="time" id="book_time" name="book_time"
       min="09:00" max="18:00" required>
    </div>

    <div class="red_button">
        Book a table
    </div>
     
  </div>
</template>

<script>
export default {
    name: 'BookTable',

}
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";

    .wrapper{
        
        input{
            width: 200px;
            padding: 10px 30px;
            border: 1px solid $dark_bg;
        }

        .number{
            position: relative;

            .fa-users{
                position: absolute;
                right: 30px;
                top: 15px;
            }
        }

        .red_button{
            color: white;
            padding: 10px 30px;
            background-color: $red_bg;
            text-transform: uppercase;
            text-align: center;
            width: 200px;
            letter-spacing: 2px;
            cursor: pointer;
        }

        .text{
            font-weight: 500;
        }
        
    }

</style>
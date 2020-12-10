<template>
    <div>
        <form>
            <!-- adding textbox input -->
            <div>
            <label>Enter Your First Name: </label>
            <!-- v-model binds value of <input type="text"> to the data entered 
            into thefirst_name property.
                Whatever u enter into the textbox will appear under 
                First Name: due to the {{}}-->
            <input type="text" v-model="first_name"/>
            <br><br>
            </div>

            <!-- adding them radio buttons -->
            <div> 
                <label>Select Your Gender: </label>
                <br>
                <input type="radio" value="Male" v-model="gender">Male
                <input type="radio" value="Female" v-model="gender">Female
                <br><br>
            </div>
            <div>
                <label>Select Your Employment Status: </label>
                <br>
                <input type="radio" value="Student" v-model="employment">Student
                <input type="radio" value="Full-time" v-model="employment">Full-time
                <input type="radio" value="Part-time" v-model="employment">Part-time
                <br><br>
            </div>

        </form>
        <!-- area to display them deets -->
        <div>
            <h3>Your Details:</h3>
            <ul>
                <li>Registered First Name: {{first_name}}</li>
                <li>Registered Gender: {{gender}}</li>
                <li>Registered Employment Status: {{employment}}</li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    data: function(){
        return {
            'first_name': '',
            'gender':'',
            // dont actually need them quotes, its to avoid confusion or something
            employment:'',

        }
    }
}
</script>
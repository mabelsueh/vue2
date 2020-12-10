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

            <!-- adding them checkboxes (returns VALUES in array for the {{}}) -->
            <div>
                <label>Check Your Interests: </label>
                <br>
                <input type="checkbox" value="Reading" v-model="interests">Reading
                <input type="checkbox" value="Sleeping" v-model="interests">Sleeping
                <input type="checkbox" value="Music" v-model="interests">Music
                <input type="checkbox" value="Television" v-model="interests">Television
                <br><br>
            </div>
            <div>
                <label> Check Your Leisure Activities: </label>
                <br>
                <input type="checkbox" value="Sports" v-model="leisure">Sports
                <input type="checkbox" value="Reading" v-model="leisure">Reading
                <input type="checkbox" value="Sleeping" v-model="leisure">Sleeping
                <input type="checkbox" value="Eating" v-model="leisure">Eating
                <input type="checkbox" value="Hanging" v-model="leisure">Hanging Out
                <br><br>
            </div>

            <!-- adding option value selector (select one only)-->
            <div>
                <label>How Did You Discover Us?</label>
                <br>
                <select v-model="hearAbout">
                    <option value="Friends">Friends</option>
                    <option value="Facebook">Facebook</option>
                    <option value="Email">From Email</option>
                </select>
            </div>
        </form>
        <!-- area to display them deets -->
        <div>
            <h3>Your Details:</h3>
            <ul>
                <li>Registered First Name: {{first_name}}</li>
                <li>Registered Gender: {{gender}}</li>
                <li>Registered Employment Status: {{employment}}</li>
                <li>Registered Interests: {{interests}}</li>
                <li>Registered Leisure Activities: {{leisure}}</li>
                <li>Registered Survey: {{hearAbout}}</li>
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
            // need to put in array cause of multi option
            interests: [],
            leisure: [],
            hearAbout: '',
        }
    }
}
</script>
<script>
    // @ts-nocheck
    
        function validateForm(event) {
    
            
            // Get the input field value
            var inputField1 = document.getElementById("fname").value;
            var inputField2 = document.getElementById("lname").value;
            var inputField3 = document.getElementById("email").value;
            var inputField4 = document.getElementById("message").value;
    
            // Check if the input field is empty
            if (inputField1 === "" || inputField2 === "" || inputField3 === "" || inputField4 === "") {
                // Prevent the form from submitting
                event.preventDefault();
                alert("Please fill in all required fields!");
            }
        }
        
    </script>
    

<form
  action="https://formspree.io/f/mlggekak#formID"
  method="POST"
  id="formID"
  on:submit={validateForm}
>
<section id="contact" class="section">
    <div id="formdetails">

        <div class="formcolumn" id="formfields">

            <label for="fname">First Name:</label><br/><hr>
            <input type="text" id="fname" name="fname"><br><br>

            <label for="lname">Last Name:</label><br /><hr>
            <input type="text" id="lname" name="lname"><br><br>
            
            <label for="email">Email:</label><br /><hr>
            <input type="text" id="email" name="email"><br><br>

            <label for="message">Message:</label><br /><hr>
            <!-- svelte-ignore element_invalid_self_closing_tag -->
            <textarea id="message" name="message" /><br><br>

        </div>

        <div class="formcolumn" id="formservices">

            <label for="service">Service</label><br/><hr>

            <div id="checkboxes">

                <div class="check">
                    <input type="checkbox" class="servicebox" name="General Inquiry">General Inquiry<br />
                </div>
                <div class="check">
                    <input type="checkbox" class="servicebox" name="IoT Project">IoT Project<br />
                </div>
                <div class="check">
                    <input type="checkbox" class="servicebox" name="XR Development">XR Development<br />
                </div>
                <div class="check">
                    <input type="checkbox" class="servicebox" name="Cloud Services">Cloud Services<br />
                </div>
                <div class="check">
                    <input type="checkbox" class="servicebox" name="Hardware/Data Integration">Hardware/Data Integration<br />
                </div>
                <div class="check">
                    <input type="checkbox" class="servicebox" name="Consultation">Consultation<br />
                </div>
                <div class="check">
                    <input type="checkbox" class="servicebox" name="Other">Other<br />
                </div>

            </div>
                   
            <br /><br />
            
            <div id="submitbutton">
                <input type="submit" id="submit" name="submit" value="Send"><br />         
            </div>

        </div>
    </div>


</section>
</form>

<style>

label
{
    font-size:2vw;
}

#submit
{
    width:6rem;
    aspect-ratio:2.5;
    
    border-radius:5vw;

    font-size:1vw;

    background-color:whitesmoke; 

}

#formfields
{
    line-height:2.25vh;
}

#formservices
{
    line-height:4vh;
    font-size:1.1rem;
}

label
{
	font-size: 1.4rem !important;
}

.formcolumn
{
    width:40%;
    color:var(--color-dark-primary);
}

.servicebox
{
    margin-right:0.7vw;
    transform:scale(1);
}

input[type=text]
{

    border-radius:.4rem;

    padding-left:1vw;

    width:100%;
    aspect-ratio:12;  

    font-size:1rem !important;

    background-color:whitesmoke; 

}

textarea
{

    padding-left:0.5vw;
    border-radius:1vw;

    width:100%;
    height:4vw;    

    font-size:1rem !important;

    background-color:whitesmoke; 

}

#formID
{
	width:100%;

	display:flex;
	justify-content: center;
	align-items: center;

}

.section
{
    font-size:1.5rem;
	width:100%;

	display:flex;
	justify-content: center;
	align-items: center;
}

#formdetails
{
    
    width:90%;
    aspect-ratio:2;

    padding-top:5vw;
    
    border-style:solid;
    border-radius:1rem;
    border-color:var(--color-light-secondary);
    border-width:.25vw;

    display:flex;
    justify-content:space-evenly;
    align-items:flex-start;

    box-shadow: 1px 1px 1px 1px rgb(0, 0, 0, 1);
}

@media(max-width:600px)
{

    #formdetails
    {
        flex-direction:column;
    }
    .formcolumn
    {
        margin-left:auto;
        margin-right:auto;
        width:80%;
    }
    #submitbutton
    {
        width:30%;
        margin-left:auto;
        margin-right:auto;
        padding-bottom:3%;
    }
    #submit
    {
        width:20vw;
        aspect-ratio:4;
        font-size:2vw;
    }
    .servicebox
    {
        width:6vw;
        height:10vw;
    }
    #formservices
    {
        font-size:3vw;
    }
    .check
    { 
        display:flex;
        align-items:center;
    }

}

</style>
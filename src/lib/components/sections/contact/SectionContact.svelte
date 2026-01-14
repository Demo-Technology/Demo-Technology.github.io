<script lang="ts">
    // @ts-nocheck
    import { inView } from '$lib/actions/animations';
	function validateForm(event: Event) {
		// Get the input field value
		var inputField1 = document.getElementById('fname').value;
		var inputField2 = document.getElementById('lname').value;
		var inputField3 = document.getElementById('email').value;
		var inputField4 = document.getElementById('message').value;

		// Check if the input field is empty
		if (inputField1 === '' || inputField2 === '' || inputField3 === '' || inputField4 === '') {
			// Prevent the form from submitting
			event.preventDefault();
			alert('Please fill in all required fields!');
		}
	}
</script>

<div class="contact">
	<section id="contact">
        <div use:inView class="animate from-top" style="margin-bottom: 2rem;">
            <h1 class="section-text-title">Contact Us</h1>
            <p class="section-text-content">We would love to hear from you! Please fill out the form below to get in touch with us.</p>
        </div>
		<form
			action="https://formspree.io/f/mlggekak#formID"
			method="POST"
			id="formID"
			on:submit={validateForm}
            use:inView
            class="animate"
		>
			<div class="form-details">
				<div class="form-column section-text-content">
                    <div class="form-entry">
                        <label for="fname">First Name:</label>
                        <input type="text" id="fname" name="fname" />
                    </div>
                    <div class="form-entry">
                        <label for="lname">Last Name:</label>
                        <input type="text" id="lname" name="lname" />
                    </div>
                    <div class="form-entry">
                        <label for="email">Email:</label>
                        <input type="text" id="email" name="email" />
                    </div>
                    <div class="form-entry">
                        <label for="message">Message:</label>
                        <textarea id="message" name="message"></textarea>
                    </div>
				</div>
				<div class="form-column section-text-content">
                    <div class="form-entry" style="justify-content: center;">
                        <label for="service" style="font-size: 1.75rem; font-weight: bold;">Service</label>
                        <div class="check-entry">
                            <input type="checkbox" name="General Inquiry" />
                            <span>General Inquiry</span>
                        </div>
                        <div class="check-entry">
                            <input type="checkbox" name="IoT Project" />
                            <span>IoT Project</span>
                        </div>
                        <div class="check-entry">
                            <input type="checkbox" name="XR Development" />
                            <span>XR Development</span>
                        </div>
                        <div class="check-entry">
                            <input type="checkbox" name="Cloud Services" />
                            <span>Cloud Services</span>
                        </div>
                        <div class="check-entry">
                            <input type="checkbox" name="Hardware/Data Integration" />
                            <span>Hardware/Data Integration</span>
                        </div>
                        <div class="check-entry">
                            <input type="checkbox" name="Consultation" />
                            <span>Consultation</span>
                        </div>
                        <div class="check-entry">
                            <input type="checkbox" name="Other" />
                            <span>Other</span>
                        </div>
                    </div>
					<div>
						<input type="submit" class="submit" name="submit" value="Submit Message" />
					</div>
				</div>
			</div>
		</form>
	</section>
</div>

<style>
    h1 {
		text-align: center;
	}

    .section-text-title {
        color: var(--color-light-primary) !important;
    }

    .section-text-content {
        color: var(--color-light-primary) !important;
    }

    .contact {
		width: 100%;
		background-color: var(--color-dark-secondary);
        border-top: 1px solid var(--color-dark-secondary);
        box-shadow: 0px -1px 5px rgba(0, 0, 0, 0.5);
		text-align: center;
        color: var(--color-light-primary) !important;
	}

    form {
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .form-details {
        max-width: 960px;
        width: 100%;
        border-radius: 1rem;
        border-width: 0.15rem;
        border-style: solid;
        padding: 3rem;
        display: grid;
		grid-template-columns: 1fr 18rem;
        gap: 6rem;
        align-items: center;
    }

    .form-column {
        display: flex;
        flex-direction: column;
        gap: 0.5rem;
        height: 100%;
        justify-content: space-between;
	}

    .form-entry {
        display: grid;
        gap: 0.25rem;
    }

    .form-entry input {
		border-radius: 0.5rem;
		font-size: 1.25rem !important;
		background-color: var(--color-light-primary);
        padding: 0.5rem;
        font-family: 'Futura Bk BT', system-ui, sans-serif;
        color: var(--color-dark-primary);
	}

    .form-entry textarea {
		border-radius: 0.5rem;
        height: 8rem;
        font-size: 1.25rem !important;
        background-color: var(--color-light-primary);
        padding: 0.5rem;
        font-family: 'Futura Bk BT', system-ui, sans-serif;
        color: var(--color-dark-primary);
	}

    .check-entry {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: flex-start;
    }

    .check-entry input {
        margin-right: 1rem;
        width: auto;
        height: auto;
    }

    .submit {
		border-radius: 1rem;
		font-size: 1.5rem !important;
		background-color: var(--color-light-primary);
        padding: 0.5rem 1.5rem;
        font-family: 'Futura Bk BT', system-ui, sans-serif;
        color: var(--color-dark-primary);
        transition: background-color 0.2s, color 0.2s;
	}

    .submit:hover {
        cursor: pointer;
        background-color: var(--color-light-secondary);
        color: var(--color-light-primary);
    }

    @media (max-width: 74rem) {
		.form-details {
			grid-template-columns: 1fr;
			gap: 2rem;
		}

        .submit {
            margin-top: 2rem;
        }
	}
</style>

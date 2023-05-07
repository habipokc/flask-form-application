# flask-form-application
This code creates a simple Flask web application that includes a web form. The form prompts the user to enter their first name and last name. When the form is submitted, the user is redirected to a success page where a personalized thank-you message is displayed.

The application uses the Flask framework along with the Flask-WTF extension for form handling. It defines a FlaskForm subclass named MyForm that represents the form fields (first name, last name) and the submit button. The DataRequired validator is applied to each field to ensure that they are not left empty.

The main routes of the application are:

The / route, which supports both GET and POST requests. When the route is accessed via GET, the form is rendered using the index.html template and an instance of MyForm. When the form is submitted, the validate_on_submit() method is called to validate the form data. If the form is valid, the first name and last name values are retrieved, and the user is redirected to the success route. If the form is not valid, the template is rendered again, showing any validation error messages.

The /success/<first_name>/<last_name> route, which displays a thank-you message to the user. The first name and last name values are received as parameters and incorporated into the message.

The application is run in debug mode using app.run(debug=True), which provides detailed error messages during development.

This code serves as a basic example of how to create a form and handle form submissions using Flask. It can be used as a starting point for building more complex web applications with form functionality.

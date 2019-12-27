1_normal form validation with jquery Validation

Step:1
html:5 Enter and in <head> section

1. provide link for Bootstap CSS &&& 2. Script for jQuery
2. For Bootstarap jquery Note Bootstap.js uses jQuery so keep jQuery just above it
3. For Jquery Validation, It uses jQuery so keep jQuery above it
4. Provide css within style for error message in .error classs
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <!--1.  For Bootstap CSS -->
           <link href="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/3.3.5/css/bootstrap.min.css" rel="stylesheet" />
   <!--2. For jquery  -->
           <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>
   <!--3. For Bootstarap with jquery Note Bootstap.js uses jQuery so keep jQuery just above it  -->
           <script src="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/3.3.5/js/bootstrap.min.js"></script>
   <!--4.  For Jquery Validation , It uses jQuery so keep jQuery above it   -->
           <script src="https://cdn.jsdelivr.net/jquery.validation/1.16.0/jquery.validate.min.js"></script>

5. Provide css within style for error message in .error classs
    <style>
   . error {color: red;}    
     </style>

  </head>

<body>

Step2:

Write the code for data entry within form also write jquery validation code within script just after close tag of </form>
which is given below
Note: Form id must be matched with jquery validation id

<form id="madhuFormValidation" method="post" action="formSubmitMessage.html">
 $('#madhuFormValidation').validate({

<h2>1_normal form validation with jquery Validation</h2>
    
<form id="madhuFormValidation" method="post" action="formSubmitMessage.html">
  <div>
    <label for="fname">First Name:</label>
    <input type="text" id="fname" name="fname"></input>
  </div>
  <div>
    <label for="lname">Last Name:</label>
    <input type="text" id="lname" name="lname"></input>
  </div>
  <div>
    <label for="user_email">Email:</label>
    <input type="email" id="user_email" name="user_email"></input>
  </div>
  <div>
    <label for="psword">Password:</label>
    <input type="password" id="psword" name="psword"></input>
  </div>
  <div>
    <input type="submit" value="Submit" />
  </div>
</form>

// For jquery Validation

<script>

  $(document).ready(function () {

   $('#madhuFormValidation').validate({
      rules: {
        fname: 'required',
        lname: 'required',
        user_email: {
          required: true,
          email: true,
        },
        psword: {
          required: true,
          minlength: 8,
        }
      },
      messages: {
        fname: 'Madhu, First Name  is required',
        lname: 'Madhu, Last Name  is required',
        user_email: {
                    required:'Madhu, Email  is required',
                    email   : "Madhu , Plz enter valid email"
        },
        psword: {
          required: 'Madhu, Password  is required',
          minlength: 'Madhu, Password must be at least 8 characters long'
        }
      },
// If we want to make the label and input field both in red color
      highlight: function (element) {
       $(element).parent().addClass('error')
     },
     unhighlight: function (element) {
       $(element).parent().removeClass('error')
     }



// // If we want to make only the  input field both in red color
//       highlight: function (element) {
//        $(element).addClass('error')
//      },
//      unhighlight: function (element) {
//        $(element).removeClass('error')
//      }


    });

  });

</script>
  </body>
</html>
 
2_bootstrap popupmodal form validation with jquery Validation
Step:1  is same as above
<body>

Step:2  
1 Make a triggering button for modal data-target="#exampleModal" which must be match with div id of modal i.e
…………………………………………………….Triggering Button data-target="#exampleModal"…………………………………..
<button type="button" class="btn btn-primary" data-toggle="modal" data-target="#exampleModal">
Launch demo modal with jquery Validation inside modal
</button>
…………………………………………………Modal <div id="exampleModal" …………………………………………………………………………………..

<div class="modal fade" id="exampleModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel"
        aria-hidden="true">
Step3:

Write the code for data entry within form also write jquery validation code within script just after close tag of </form>
which is given below
Note: Form id must be matched with jquery validation id

<form id="madhuFormValidation" method="post" action="formSubmitMessage.html">
 $('#madhuFormValidation').validate({

   <!-- ==================Modal Part Start============= -->

    <!-- 1 Make a triggering button for modal  -->
    <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#exampleModal">
        Launch demo modal with jquery Validation inside modal
    </button>

    <!—Pop up Modal Modal -->
    <div class="modal fade" id="exampleModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel"
        aria-hidden="true">
        <div class="modal-dialog" role="document">
            <div class="modal-content">
                <div class="modal-header">
                    <h2 class="modal-title" id="exampleModalLabel">2_bootstrap popupmodal form validation with jquery Validation

</h2>
                    <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                        <span aria-hidden="true">&times;</span>
                    </button>
                </div>
                <div class="modal-body">
                    <!-- ==========================Form Code with Jquery Validation Script Start================== -->

<form id="madhuFormValidation" method="post" action="formSubmitMessage.html">
    <div>
        <label for="fname">First Name:</label>
        <input type="text" id="fname" name="fname"></input>
    </div>
    <div>
        <label for="lname">Last Name:</label>
        <input type="text" id="lname" name="lname"></input>
    </div>
    <div>
        <label for="user_email">Email:</label>
        <input type="email" id="user_email" name="user_email"></input>
    </div>
    <div>
        <label for="psword">Password:</label>
        <input type="password" id="psword" name="psword"></input>
    </div>
    <div>
        <input type="submit" value="Submit" />
    </div>
</form>

// For jquery Validation

<script>

    $(document).ready(function () {

        $('#madhuFormValidation').validate({
            rules: {
                fname: 'required',
                lname: 'required',
                user_email: {
                    required: true,
                    email: true,
                },
                psword: {
                    required: true,
                    minlength: 8,
                }
            },
            messages: {
                fname: 'Madhu, First Name  is required',
                lname: 'Madhu, Last Name  is required',
                user_email: {
                    required: 'Madhu, Email  is required',
                    email: "Madhu , Plz enter valid email"
                },
                psword: {
                    required: 'Madhu, Password  is required',
                    minlength: 'Madhu, Password must be at least 8 characters long'
                }
            },
            // // If we want to make the label and input field both in red color
            //       highlight: function (element) {
            //        $(element).parent().addClass('error')
            //      },
            //      unhighlight: function (element) {
            //        $(element).parent().removeClass('error')
            //      }

            // If we want to make only the  input field both in red color
            highlight: function (element) {
                $(element).addClass('error')
            },
            unhighlight: function (element) {
                $(element).removeClass('error')
            }

        });

    });

</script>

                    <!-- ==========================Form Code with Jquery Validation Script End================== -->
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
                    <button type="button" class="btn btn-primary">Save changes</button>
                </div>
            </div>
        </div>
    </div>
    <!-- ==================Modal Part End============= -->

</body>

</html>

3_modalform validation by jquery plugin from remote next page
Step:1 is same as above

<body>

Step:2  
1 Make a triggering button for modal data-target="#exampleModal" which must be match with div id of modal
2 by using href=”Link of popup modal in next page can be given” href="3_1remotePage.html"

…………………………………………………….Triggering Button data-target="#exampleModal"…………………………………..
<a
            href="3_1remotePage.html"
            class="btn btn-primary"
            data-toggle="modal"
            data-target="#exampleModal"
        >
Launch demo modal with jquery Validation inside modal publishing modal
from remote next page
</a>

…………………………………………………Modal <div id="exampleModal" …………………………………………………………………………………..

<div
            class="modal fade"
            id="exampleModal"
            tabindex="-1"
            role="dialog"
            aria-labelledby="exampleModalLabel"
            aria-hidden="true"
        >

Step:3

Write only up to <modal content > here in this modal page
and write
<modal header> <modal body> <modal footer>
part in remote page (we will write code of form to enter data and jquery validation in remote page look step 4 for remote page )

-------<!-- ==================Modal Part Start============= -->

        <!-- Button trigger modal -->
        <a
            href="3_1remotePage.html"
            class="btn btn-primary"
            data-toggle="modal"
            data-target="#exampleModal"
        >
            Launch demo modal with jquery Validation inside modal publishing modal
            from remote next page
        </a>

        <!-- Modal -->
        <div
            class="modal fade"
            id="exampleModal"
            tabindex="-1"
            role="dialog"
            aria-labelledby="exampleModalLabel"
            aria-hidden="true"
        >
            <div class="modal-dialog" role="document">
                <div class="modal-content">
                    <!-- ..................Cut all code from here and pasete it in 3_1remotePage.html  -->
                </div>
            </div>
        </div>
        <!-- ==================Modal Part End============= -->
    </body>

</html>

Step:4 (Remote Page )
Write the code starting from <modal header > …………………………<modal body>
Actually we are in Modal page itself so no need to write any bootstrap css, jquery validation link here we can directly use here .
Write the code for data entry within form in <modal body section> also write jquery validation code within script just after close tag of </form>
Note: Form id must be matched with jquery validation id

<form id="madhuFormValidation" method="post" action="formSubmitMessage.html">
 $('#madhuFormValidation').validate({

Look step 4 for remote page code

We can write code to give color for error class within here

<style>
    .error {
        color: red;
    }
</style>

The overall code is given below:

<style>
    .error {
        color: red;
    }
</style>
<div class="modal-header">
    <h2 class="modal-title" id="exampleModalLabel">3_modalform validation by jquery plugin from remote next page
    </h2>
    <button type="button" class="close" data-dismiss="modal" aria-label="Close">
        <span aria-hidden="true">&times;</span>
    </button>
</div>
<div class="modal-body">
    <!-- ==========================Form Code with Jquery Validation Script Start================== -->

    <form id="madhuFormValidation" method="post" action="formSubmitMessage.html">
        <div>
            <label for="fname">First Name:</label>
            <input type="text" id="fname" name="fname"></input>
        </div>
        <div>
            <label for="lname">Last Name:</label>
            <input type="text" id="lname" name="lname"></input>
        </div>
        <div>
            <label for="user_email">Email:</label>
            <input type="email" id="user_email" name="user_email"></input>
        </div>
        <div>
            <label for="psword">Password:</label>
            <input type="password" id="psword" name="psword"></input>
        </div>
        <div>
            <input type="submit" value="Submit" />
        </div>
    </form>

// For jquery Validation
<script>

        $(document).ready(function () {

            $('#madhuFormValidation').validate({
                rules: {
                    fname: 'required',
                    lname: 'required',
                    user_email: {
                        required: true,
                        email: true,
                    },
                    psword: {
                        required: true,
                        minlength: 8,
                    }
                },
                messages: {
                    fname: 'Madhu, First Name  is required',
                    lname: 'Madhu, Last Name  is required',
                    user_email: {
                        required: 'Madhu, Email  is required',
                        email: 'Madhu , Plz enter valid email',
                    },
                    psword: {
                        required: 'Madhu, Password  is required',
                        minlength: 'Madhu, Password must be at least 8 characters long',
                    }
                },

                // If we want to make the label and input field both in red color
                      highlight: function (element) {
                       $(element).parent().addClass('error')
                     },
                     unhighlight: function (element) {
                       $(element).parent().removeClass('error')
                     }



                // // If we want to make only the  input field both in red color
                // highlight: function (element) {
                //     $(element).addClass('error')
                // },
                // unhighlight: function (element) {
                //     $(element).removeClass('error')
                // }

            });

        });

    </script>

    <!-- ==========================Form Code with Jquery Validation Script End================== -->

</div>
<div class="modal-footer">
    <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
    <button type="button" class="btn btn-primary">Save changes</button>
</div>
Happy Coding

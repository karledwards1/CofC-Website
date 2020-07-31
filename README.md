# cofc-website

This is the HTML that I’ve added to the Center For Entrepreneurship home page.
All CSS and JavaScript I wrote had to be inline (obviously terrible practice but
our CASCADE service - at least at the time - wouldn't allow 'programatic' changes
by any other method).

I put all of the faculty names in the dropdown inside <a></a> tags in case anybody
wants to link names to blurbs in the future. We talked about this before but were
not able to get interviews in time to commit.

Everything I changed should be self explanatory... I changed **a lot** of pictures
in to editable content (pngs of text and stuff like that). The faculty and staff 
page really needs to be published ASAP but there are still a handful of people I 
wasn't able to get pictures from. Once the pictures are there it should be good to go.

## **These buttons cannot be edited directly from the UI view in CASCADE!**

From the normal editing window there is a small html button on the toolbar to access
the child code. To edit these buttons scroll to the bottom of the html popup window.

```
<!-- CSS For Dropdown Buttons —>
<style media=“screen">
  /* Dropdown Button */
  .dropbtn {
    background-color: #660000;
    border: none;
    border-radius: 1em !important;
    box-shadow: none;
    color: #fff;
    cursor: pointer;
    display: inline-block;
    font-size: 1rem;
    font-weight: bold;
    line-height: 1.5;
    margin: 1.5%;
    min-width: 230px;
    opacity: 1;
    padding: 0.375rem 1.75rem;
    text-align: center;
    text-shadow: none;
    text-transform: none;
    transition: color 0.15s ease-in-out, background-color 0.15s ease-in-out, border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out;
    user-select: none;
    vertical-align: middle;
    width: 50%;
    -webkit-border-radius: 1em !important;
    -moz-border-radius: 1em !important;
    -ms-border-radius: 1em !important;
  }

  /* Dropdown button on hover & focus */
  .dropbtn:hover {
    color: #a79e70;
  }

  .dropbtn:hover,
  .dropbtn:focus {
    outline: none;
  }

  /* Container needed to position the dropdown content */
  .dropdown {
    display: inline-block;
    margin: auto 5%;
    position: relative;
  }

  /* Dropdown Content (Hidden by Default) */
  .dropdown-content {
    background-color: white;
    border: solid 1px #660000;
    border-radius: 1rem;
    box-shadow: none;
    display: none;
    line-height: 1.5;
    margin: 1.5%;
    min-height: 1px;
    min-width: 230px;
    padding: 0.375rem 0;
    position: absolute;
    text-align: left;
    width: 50%;
    z-index: 1;
  }

  /* Links inside the dropdown */
  .dropdown-content a {
    color: black;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
  }

  /* Change color of dropdown links on hover */
  .dropdown-content a:hover {
    color: #a79e70
  }

  /* Show the dropdown menu */
  .show {
    display: block;
  }

  .tooltip {
    display: inline-block;
    position: relative;
  }

  .tooltip .tooltiptext {
    background-color: #a79e70;
    border-radius: 1rem;
    color: #fff;
    margin: 1.5%;
    min-width: 200px;
    padding: 0.375rem 0;
    position: absolute;
    right: 105%;
    text-align: center;
    top: -5px;
    visibility: hidden;
    /* width: 120px; */
    z-index: 1;
  }

  .tooltip:hover .tooltiptext {
    visibility: visible;
  }
</style>

<!-- Dropdown Content -->
<center>
  <div class="dropdown">
    <button onclick="toggleAdvBrdDrpDwn()" class="dropbtn">Advisory Board</button>
    <div id="advBrdDrpDwn" class="dropdown-content">
      <a class="tooltip" href="#">
        Mark Richards
        <span class="tooltiptext">This is Mark Richard's bio</span>
      </a>
      <a class="tooltip" href="#">
        Michael Cahill
        <span class="tooltiptext">This is Michael Cahill's bio</span>
      </a>
      <a class="tooltip" href="#">
        Jennifer Garr
        <span class="tooltiptext">This is Jennifer Garr's bio</span>
      </a>
      <a class="tooltip" href="#">
        Jerry Nairne
        <span class="tooltiptext">This is Jerry Nairne's bio</span>
      </a>
      <a class="tooltip" href="#">
        Neely Powell
        <span class="tooltiptext">This is Neely Powell's bio</span>
      </a>
      <a class="tooltip" href="#">
        Lisa Quadrini
        <span class="tooltiptext">This is Lisa Quadrini's bio</span>
      </a>
      <a class="tooltip" href="#">
        Glenn Starkman
        <span class="tooltiptext">This is Glenn Starkman's bio</span>
      </a>
      <a class="tooltip" href="#">
        Stewart Vernon
        <span class="tooltiptext">This is Stewart Vernon's bio</span>
      </a>
      <a class="tooltip" href="#">
        Stuart Williams
        <span class="tooltiptext">This is Stuart Williams' bio</span>
      </a>
    </div>
  </div>

  <div class="dropdown">
    <button onclick="toggleProfDrpDwn()" class="dropbtn">ENTR Professors</button>
    <div id="profDrpDwn" class="dropdown-content">
      <a href="#">David Wyman</a>
      <a href="#">Lancie Affonso</a>
      <a href="#">David Desplaces</a>
      <a href="#">David Hansen</a>
      <a href="#">Kelly Shaver</a>
      <a href="#">Chris Starr</a>
    </div>
  </div>
</center>
<!-- END -->

<!-- JavaScript for Dropdown Buttons -->
<script type="text/javascript">
  // When the user clicks on the button, toggle between hiding and showing the dropdown content
  function toggleAdvBrdDrpDwn() {
    document.getElementById("advBrdDrpDwn").classList.toggle("show");
  }

  function toggleProfDrpDwn() {
    document.getElementById("profDrpDwn").classList.toggle("show");
  }

  // Close the dropdown menu if the user clicks outside
  window.onclick = function(event) {
    if (!event.target.matches('.dropbtn')) {
      var dropdowns = document.getElementsByClassName("dropdown-content");
      var i;
      for (i = 0; i < dropdowns.length; i++) {
        var openDropdown = dropdowns[i];
        if (openDropdown.classList.contains('show')) {
          openDropdown.classList.remove('show');
        }
      }
    }
  }
</script>
```

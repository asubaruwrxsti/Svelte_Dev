<script>
    import App from "../App.svelte";

window.addEventListener("DOMContentLoaded", (event) => {
    const form = document.getElementById("login_form");
    form.addEventListener("submit", (event) => {
        event.preventDefault();
        const username = document.getElementById("exampleInputEmail1").value;
        const password = document.getElementById("exampleInputPassword1").value;
        fetch("http://localhost:5000/login", {
            method: "POST",
            headers: {
                "Content-Type": "application/json",
                "Access-Control-Allow-Origin": "*",
                "mode": "no-cors",
            },
            body: JSON.stringify({ username, password }),
          });
        });
});
</script>

<form id="login_form" class="d-flex p-2 flex-column align-items-center mt-3 mb-3">
    <div class="form-group">
      <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Username">
    </div>
    <div class="form-group mt-3">
      <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
    </div>
    <button type="submit" class="btn btn-primary mt-3">Submit</button>
</form>
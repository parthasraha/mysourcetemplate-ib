<!DOCTYPE html>
<html>
<head>
  <title>A static website</title>

  <!-- include the widget -->
  <script type="text/javascript" src="https://identity.netlify.com/v1/netlify-identity-widget.js"></script>
</head>
<body>
    <script>
    if (window.netlifyIdentity) {
        window.netlifyIdentity.on("init", user => {
        if (!user) {
            window.netlifyIdentity.on("login", () => {
            document.location.href = "/admin/";
            });
        }
        });
    }
    </script>
</body>
</html>
document.addEventListener("DOMContentLoaded", () => {
  // Suporte
  const btnSuporte = document.getElementById("btn-suporte");
  if (btnSuporte) {
    btnSuporte.addEventListener("click", () => {
      const email = document.getElementById("emailSuporte").value.trim();
      const mensagem = document.getElementById("mensagem").value.trim();
      const status = document.getElementById("suporte-status");

      if (!email || !mensagem) {
        status.textContent = "Preenche o email e a mensagem antes de enviar.";
        status.style.color = "#dc2626";
        return;
      }

      status.textContent = "Pedido enviado! Vamos responder por email em breve.";
      status.style.color = "#16a34a";
    });
  }

  // Login
  const btnLogin = document.getElementById("btn-login");
  if (btnLogin) {
    btnLogin.addEventListener("click", () => {
      const email = document.getElementById("emailLogin").value.trim();
      const pass = document.getElementById("passwordLogin").value.trim();
      const status = document.getElementById("login-status");

      if (!email || !pass) {
        status.textContent = "Preenche email e password.";
        status.style.color = "#dc2626";
        return;
      }

      // Simulação de login
      status.textContent = "Login simulado com sucesso (frontend).";
      status.style.color = "#16a34a";
    });
  }
});

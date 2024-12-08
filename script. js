document.addEventListener("DOMContentLoaded", function () {
    const form = document.getElementById("contactForm");

    form.addEventListener("submit", async (e) => {
        e.preventDefault(); // Prevent the default form submission

        // Collect form data
        const message = document.getElementById("message").value;
        const email = document.getElementById("email").value;

        const data = { message, email };

        try {
            const response = await fetch(
                "https://script.google.com/macros/s/AKfycbzt9eCcok17VeRmhUyFxJf5tfif4F9OfVyxA56jfbV0A3pgPQHqaHvZ6kCLmp82ppNV/exec",
                {
                    method: "POST",
                    headers: {
                        "Content-Type": "application/json",
                    },
                    body: JSON.stringify(data), // Send data as JSON
                }
            );

            const result = await response.json();
            if (result.success) {
                alert("Message sent successfully!");
            } else {
                alert("Error: " + result.error);
            }
        } catch (error) {
            console.error("Error details:", error);
            alert("Error sending the message. Please try again later.");
        }
    });
});

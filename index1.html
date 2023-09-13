<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chatbot GymBulk</title>
    <script src="https://cdn.jsdelivr.net/npm/gradio@2.2.12/dist/gradio.min.js"></script>
</head>
<body>
    <div id="chatbot-interface"></div>
    <script>
        // Charger la clé API depuis un fichier (à adapter)
        const apiKey = "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";

        const message_history = [
            {"role": "user", "content": "Tu es un bot de l'entreprise GymBulk spécialisé dans la transformation physique. Tu es conçu pour aider les personnes à trouver des recettes ou encore des équivalences nutritionnelles. Tu commenceras chaque discussion par : Bonjour, je suis l'assistant GymBulk. Comment puis-je t'aider ?"},
            {"role": "assistant", "content": "Ok, je vais faire de mon mieux"}
        ];

        function predict(input) {
            message_history.push({"role": "user", "content": input});

            fetch("https://api.openai.com/v1/engines/gpt-3.5-turbo/completions", {
                method: "POST",
                headers: {
                    "Content-Type": "application/json",
                    "Authorization": `Bearer ${apiKey}`
                },
                body: JSON.stringify({
                    messages: message_history
                })
            })
            .then(response => response.json())
            .then(data => {
                const reply_content = data.choices[0].message.content;
                message_history.push({"role": "assistant", "content": reply_content});
                const response = message_history.slice(2).filter((_, i) => i % 2 === 0);
                grInterface.postMessage({response});
            });
        }

        const grInterface = gr.Interface(
            predict,
            "textbox",
            "textbox",
            {
                examples: [["Recette de lasagnes", "Voici la recette des lasagnes..."]],
                style: "panel",
                label: "Envoyer votre message",
                placeholder: "Saisissez votre message ici",
                input_type: "text",
                max_length: 150,
                submit_text: "Envoyer",
                server: "https://api.openai.com",
                token: apiKey
            }
        );

        grInterface.launch();
    </script>
</body>
</html>

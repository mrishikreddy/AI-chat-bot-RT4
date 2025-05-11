# AI Chatbot

A modern AI-powered chatbot application built with Next.js, designed to handle user queries by interfacing with the Gemini 2.0 Flash API. The chatbot sends user prompts to the API and displays responses in a sleek, user-friendly interface.

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [API Details](#api-details)
- [Rate Limits](#rate-limits)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
- [Acknowledgements](#acknowledgements)

## Features
- Real-time query processing with Gemini 2.0 Flash API.
- Responsive and modular UI built with Next.js and CSS modules.
- Efficient API endpoint for handling AI prompt submissions.
- Scalable architecture for future enhancements.

## Technologies Used
- **Next.js**: React framework for server-side rendering and API routes.
- **Gemini 2.0 Flash API**: Powers the AI response generation.
- **CSS Modules**: Scoped styling for the frontend.
- **Node.js**: Runtime for the development environment.
- **Vercel**: Recommended for deployment (optional).

## Project Structure
```
AI-Chatbot/
├── src/
│   ├── app/
│   │   ├── page.js              # Main page logic for query handling and UI
│   │   ├── page.module.css      # Styles for the main page
│   ├── api/
│   │   ├── aiEndPoint/
│   │   │   ├── route.js         # API route for Gemini 2.0 Flash integration
├── package.json                 # Project dependencies and scripts
├── README.md                    # This file
```

- **`/src/app/page.js`**: Contains the core logic for the chatbot interface, including sending queries to the API and rendering responses.
- **`/src/app/page.module.css`**: Stylesheet for the chatbot UI, using CSS modules for scoped styling.
- **`/src/app/api/aiEndPoint/route.js`**: API route that forwards user prompts to the Gemini 2.0 Flash API and returns responses.

## Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/AI-Chatbot.git
   cd AI-Chatbot
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Set up environment variables**:
   Create a `.env.local` file in the root directory and add your Gemini API key:
   ```env
   GEMINI_API_KEY=your-api-key-here
   ```

4. **Run the development server**:
   ```bash
   npm run dev
   ```
   Open [http://localhost:3000](http://localhost:3000) in your browser to view the chatbot.

## Usage
1. Navigate to the chatbot interface in your browser.
2. Enter a query in the input field.
3. The query is sent to the Gemini 2.0 Flash API via the `/api/aiEndPoint` route.
4. View the AI-generated response displayed on the page.

For testing the API directly:
```bash
curl -X POST http://localhost:3000/api/aiEndPoint -H "Content-Type: application/json" -d '{"prompt": "Hello, AI!"}'
```

## API Details
The chatbot uses the Gemini 2.0 Flash API for processing prompts:
- **Endpoint**: `/api/aiEndPoint`
- **Method**: POST
- **Request Body**:
  ```json
  {
    "prompt": "Your query here"
  }
  ```
- **Response**:
  ```json
  {
    "response": "AI-generated response"
  }
  ```

Ensure the `GEMINI_API_KEY` is correctly set in `.env.local` to authenticate API requests.

## Rate Limits
The Gemini 2.0 Flash API has the following limits:
- **Daily Limit**: 3,000 prompts per day.
- **Per-Minute Limit**: Maximum of 30 prompts per minute.

Exceeding these limits may result in temporary API unavailability. Plan your usage accordingly.

## Contributing
We welcome contributions to improve the AI Chatbot! To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Make your changes and commit (`git commit -m "Add your feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.

Please ensure your code follows the project's coding standards and includes relevant tests.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact
For questions or feedback, reach out to:
- **Email**: your-email@example.com
- **GitHub**: [your-username](https://github.com/your-username)

## Acknowledgements
- [Gemini 2.0 Flash API](https://gemini.ai) for powering the AI responses.
- [Next.js](https://nextjs.org) for the robust framework.
- The open-source community for inspiration and tools.
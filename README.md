
# ADK-TS with Next.js: Multi-Agent Demo

This project demonstrates a multi-agent architecture using [IQ's ADK](https://www.npmjs.com/package/@iqai/adk) within a [Next.js](https://nextjs.org) app. It features a root agent that delegates user requests to specialized sub-agents for jokes and weather information.

## Features

- **Root agent** orchestrates sub-agents for different domains
- **Joke agent** fetches random jokes from an external API
- **Weather agent** retrieves current weather for any city
- Modern UI with Tailwind CSS
- TypeScript, ADK, and Gemini model integration

## Project Structure

```text
src/
  agents/
    index.ts                  # Root agent setup
    sub-agents/
      joke-agent/
        agent.ts              # Joke agent definition
        tools.ts              # Joke tool implementation
      weather-agent/
        agent.ts              # Weather agent definition
        tools.ts              # Weather tool implementation
  app/
    _actions.ts               # Server actions for agent queries
    component/agent-form.tsx  # Main agent form UI
    page.tsx                  # Home page
    globals.css               # Global styles
```

## Getting Started

1. **Install dependencies:**

  ```bash
  npm install
  ```

2. **Set environment variables:**

  Create a `.env` file with:

  ```env
  GOOGLE_API_KEY=your-google-api-key
  LLM_MODEL=gemini-2.5-flash
  ```

3. **Run the development server:**

  ```bash
  npm run dev
  ```

4. **Open [http://localhost:3000](http://localhost:3000)** to use the agent interface.

## Usage

Enter a message in the agent form:

- Ask for a joke (e.g., "Tell me a joke")
- Request weather (e.g., "What's the weather in London?")

The root agent routes your request to the appropriate sub-agent.

## Tech Stack

- Next.js 15
- React 19
- TypeScript
- ADK-TS
- Tailwind CSS
- Biome (lint/format)

## Learn More

- [ADK-TS Documentation](https://adk.iqai.com/)
- [Next.js Documentation](https://nextjs.org/docs)

## License

This project is licensed under the MIT License.

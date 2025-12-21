# Design Insight Builder
[![PyPI version](https://badge.fury.io/py/design-insight-builder.svg)](https://badge.fury.io/py/design-insight-builder)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Downloads](https://static.pepy.tech/badge/design-insight-builder)](https://pepy.tech/project/design-insight-builder)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue)](https://www.linkedin.com/in/eugene-evstafev-716669181/)


Design Insight Builder is a Python package that helps users extract and organize practical design tips from text inputs. Users can input text containing design advice, and the package will process the information, identifying and structuring key design tips, techniques, and insights. The output will be a well-organized list of actionable design tips, making it easy for users to quickly grasp and apply the advice. This is particularly useful for designers, students, or anyone looking to improve their design skills by extracting valuable insights from text sources.

## Features

- Extracts and organizes design tips from text inputs.
- Uses advanced language models to process and structure information.
- Supports custom language models via LangChain.
- Easy to integrate and use in your projects.

## Installation

You can install the package using pip:

```bash
pip install design_insight_builder
```

## Usage

Here is a basic example of how to use the `design_insight_builder` package:

```python
from design_insight_builder import design_insight_builder

user_input = "Your text containing design advice goes here."
response = design_insight_builder(user_input)
print(response)
```

### Input Parameters

- `user_input` (str): The user input text to process.
- `llm` (Optional[BaseChatModel]): The LangChain LLM instance to use. If not provided, the default `ChatLLM7` will be used.
- `api_key` (Optional[str]): The API key for LLM7. If not provided, the default API key will be used.

### Using Custom Language Models

You can use custom language models from LangChain by passing an instance of `BaseChatModel`. Here are examples using different LLMs:

#### Using OpenAI

```python
from langchain_openai import ChatOpenAI
from design_insight_builder import design_insight_builder

llm = ChatOpenAI()
response = design_insight_builder(user_input, llm=llm)
print(response)
```

#### Using Anthropic

```python
from langchain_anthropic import ChatAnthropic
from design_insight_builder import design_insight_builder

llm = ChatAnthropic()
response = design_insight_builder(user_input, llm=llm)
print(response)
```

#### Using Google Generative AI

```python
from langchain_google_genai import ChatGoogleGenerativeAI
from design_insight_builder import design_insight_builder

llm = ChatGoogleGenerativeAI()
response = design_insight_builder(user_input, llm=llm)
print(response)
```

### API Key

The default rate limits for LLM7 free tier are sufficient for most use cases of this package. If you need higher rate limits for LLM7, you can pass your own API key via the environment variable `LLM7_API_KEY` or directly in the function call:

```python
response = design_insight_builder(user_input, api_key="your_api_key")
```

You can get a free API key by registering at [LLM7 Token](https://token.llm7.io/).

## Contributing

Contributions are welcome! Please open an issue or submit a pull request on [GitHub](https://github.com/chigwell/design-insight-builder).

## License

This project is licensed under the MIT License.

## Author

- **Eugene Evstafev**
- Email: [hi@euegne.plus](mailto:hi@euegne.plus)
- GitHub: [chigwell](https://github.com/chigwell)
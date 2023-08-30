# Mr-Sales-Signal

## Introduction

The `ai_sales_signal` configuration is designed to intelligently analyze articles related to sales signals and provide structured insights about them. This document explains the structure and provides instructions on how to understand the components of the configuration.

## Components

### 1. Metadata

- `name`: The name of the sales signal model.
- `version`: The current version of the model.

### 2. Analysis Input

The `analysis_input` field contains information about the article that needs to be analyzed and instructions for the analysis:

- `instructions`: Detailed steps on how the analysis should be conducted.
- `article`: Contains details about the article like `title`, `snippet`, `publisher`, `datePublished`, `articleLink`, `textContent`, and `length`.

### 3. Desired Output

`analysis_desired_output` provides a schema of what the desired output structure should look like after the analysis.

### 4. Analysis Engine

The heart of the configuration. This section dictates how the article is to be classified and reasoned upon.

#### Classification

The `classification` field is broken down into multiple categories, each with its own subcategories:

- **Signal Category**: Broad categories into which the sales signal can fall, such as:
  - Growth
  - Financial
  - People
  - Awards & Recognition
  - Events & Marketing
  - Corporate Updates
  - Negative News
  
Each of these categories further have **Signal Types** that describe specific events or updates within the category. For instance, under `Growth`, you have types like `Partnership or Joint Venture`, `New Geography`, `Fundraising`, etc.

Each Signal Type has:
- `description`: A brief explanation of the signal type.
- `api_tag`: Tags that can be used to categorize the signal in an API system or database.

#### Reasoning Frameworks

The `reasoning_frameworks` provides the methodologies used to derive insights. Currently, it has `Inductive` reasoning which helps in forming general conclusions from specific observations.

## How to Use

1. Pass the article details into the `analysis_input` field.
2. Follow the `instructions` in the `analysis_input` field to analyze the article. 
3. Use the `classification` field of the `analysis_engine` to classify the information in the article.
4. Based on the classification, use the `reasoning_frameworks` to derive inductive insights about the article.
5. Format the output according to the schema provided in `analysis_desired_output`.

## Conclusion

The `ai_sales_signal` configuration is a powerful tool for sales and marketing professionals to gain insights from articles and news. By following the provided structure and instructions, one can derive valuable information and classify sales signals effectively.

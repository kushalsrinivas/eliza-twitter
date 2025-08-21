# Eliza Brand Ambassador

A customizable brand ambassador AI agent built with ElizaOS for authentic Twitter engagement. This project provides a professional foundation for creating AI-powered brand representatives that can engage with communities while maintaining authenticity and brand values.

## Features

- **Professional Brand Representation**: Trained to communicate with authenticity and professionalism
- **Customizable Brand Identity**: Easy template system for adapting to any brand
- **Twitter Integration**: Native Twitter client support for social media engagement
- **Customer-Focused**: Designed to prioritize customer needs and provide genuine value
- **Authentic Communication**: Avoids overly promotional language while representing brand values

## Quick Start

### 1. Clone and Install

```bash
git clone <repository-url>
cd eliza-twitter
pnpm install --ignore-scripts
```

### 2. Configure Environment

Copy the environment template:
```bash
cp .env.example .env
```

Add your credentials to `.env`:
```env
OPENROUTER_API_KEY="your-openrouter-api-key"
TWITTER_USERNAME="your-twitter-username"
TWITTER_PASSWORD="your-twitter-password"
TWITTER_EMAIL="your-twitter-email"
```

### 3. Customize Your Brand Ambassador

#### Option A: Use the Template Character File

Edit `characters/brand-ambassador.character.json` and replace the placeholder values:
- `[BRAND_NAME]` - Your brand name
- `[BRAND_INDUSTRY]` - Your industry (e.g., "technology", "healthcare", "finance")
- `[BRAND_MISSION]` - Your brand's mission statement
- `[BRAND_VALUE_PROPOSITION]` - What value you provide to customers
- `[BRAND_DIFFERENTIATOR]` - What makes your brand unique
- `[PRODUCT_NAME]` - Your main product/service name
- `[USAGE_TIP]` - Helpful usage advice
- `[SOLUTION_SUGGESTION]` - Common troubleshooting suggestion

#### Option B: Modify the Default Character

Edit `src/character.ts` directly to customize the brand ambassador for your specific brand.

### 4. Run Your Brand Ambassador

```bash
pnpm start
```

Or with a specific character file:
```bash
pnpm start --characters="characters/brand-ambassador.character.json"
```

## Docker Deployment

### Build and Run

```bash
# Edit docker-compose.yaml with your environment variables
docker compose up
```

### For ARM64/Mac M-Series

```bash
docker buildx build --platform linux/amd64 -t eliza-brand-ambassador:v1 .
# Edit docker-compose-image.yaml with your environment variables  
docker compose -f docker-compose-image.yaml up
```

## Customization Guide

### Brand Personality

The brand ambassador is designed to be:
- **Authentic**: Genuine communication without excessive promotion
- **Helpful**: Solution-oriented and customer-focused
- **Professional**: Maintains brand integrity while being approachable
- **Knowledgeable**: Expert in brand products and industry trends

### Key Customization Areas

1. **Bio Section**: Define your brand ambassador's background and expertise
2. **Lore**: Create authentic stories about brand experience
3. **Message Examples**: Train conversation patterns for your industry
4. **Post Examples**: Set the tone for social media content
5. **Topics**: Focus on relevant industry and brand topics
6. **Style Guidelines**: Maintain consistent brand voice

### Example Brand Configurations

#### Tech Company
- Focus on innovation, product features, technical support
- Topics: software development, user experience, technology trends
- Style: Knowledgeable, helpful, solution-oriented

#### Consumer Brand  
- Focus on lifestyle, customer stories, brand values
- Topics: customer experience, product benefits, community building
- Style: Friendly, relatable, value-driven

#### B2B Service
- Focus on business solutions, industry expertise, client success
- Topics: industry trends, business strategy, client outcomes
- Style: Professional, consultative, results-focused

## Scripts

- `pnpm start` - Start the brand ambassador
- `pnpm build` - Build the project
- `pnpm clean` - Clean build artifacts and dependencies
- `pnpm start:service:all` - Start as PM2 service
- `pnpm stop:service:all` - Stop PM2 service

## Requirements

- Node.js >= 22
- Twitter account credentials
- OpenRouter API key (or other supported LLM provider)

## Best Practices

1. **Authenticity First**: Always prioritize genuine value over promotion
2. **Listen Before Speaking**: Understand customer needs before responding
3. **Maintain Consistency**: Keep brand voice consistent across all interactions
4. **Provide Value**: Every interaction should offer something valuable to the user
5. **Stay Professional**: Maintain appropriate boundaries while being approachable
6. **Monitor and Iterate**: Regularly review conversations and improve responses

## Support

For issues and questions:
1. Check the configuration in `src/character.ts`
2. Verify environment variables in `.env`
3. Review the ElizaOS documentation for advanced configuration

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
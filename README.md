# Budget HoloLens Vision System

A Unity-based computer vision system for HoloLens that leverages Azure Computer Vision API for object detection and visualization. The system includes caching, retry logic, and efficient resource management to optimize API usage within free tier limits.

## Features

- Azure Computer Vision integration
- Local image caching
- Holographic label creation
- Automatic retry mechanism
- Transaction limit management
- Resource cleanup handling
- Camera resolution optimization

## Prerequisites

- HoloLens device
- Unity 2020.3 or later
- Microsoft Mixed Reality Toolkit
- Azure subscription
- Required Unity packages:
  - Mixed Reality Toolkit
  - Azure Cognitive Services SDK

## Setup

1. Azure Configuration:
```json
{
    "AzureVisionApiKey": "your-api-key",
    "AzureVisionEndpoint": "your-endpoint-url"
}
```

2. Unity Project Setup:
- Import MRTK
- Add script to camera object
- Configure API credentials

## Key Components

### Vision Client
- Handles Azure API communication
- Manages authentication
- Implements retry logic

### Camera Management
- Automatic resolution selection
- Photo capture handling
- Resource cleanup

### Caching System
- 24-hour cache duration
- SHA256 image hashing
- Automatic cache cleanup

## Usage Limits

- Free tier: 5000 transactions/month
- Automatic limit monitoring
- Warning system for approaching limits

## Error Handling

- Connection retry (3 attempts)
- Exponential backoff
- Transient error detection
- Resource disposal management

## Best Practices

1. Implement CaptureImage() method
2. Configure appropriate cache duration
3. Monitor transaction counts
4. Handle disposal properly
5. Test connection at startup

## Performance Optimization

- Local processing option
- Resolution optimization
- Cache management
- Resource cleanup

## Implementation Guide

### Required Methods to Implement

```csharp
private async Task<byte[]> CaptureImage()
{
    // Implement camera capture logic
}

private void CreateHolographicLabel()
{
    // Implement MRTK visualization
}
```

## Safety Features

- Automatic resource cleanup
- Memory management
- Transaction limiting
- Error recovery

## Contributing

Feel free to submit issues and enhancement requests!

## License

[Specify your license here]

## Acknowledgments

- Microsoft Mixed Reality Team
- Azure Computer Vision Team
- Unity Technologies

## Known Limitations

- Free tier restrictions
- Cache memory usage
- Processing latency
- Network dependency

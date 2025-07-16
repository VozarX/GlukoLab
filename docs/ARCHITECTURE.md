# GlukoLab Architecture Proposal

This document outlines a possible architecture for the GlukoLab Android application. The goal is to keep the codebase modular and easy to maintain while supporting a modern, minimalist user experience.

## Technology stack

- **Programming language**: Kotlin
- **UI framework**: [Jetpack Compose](https://developer.android.com/jetpack/compose)
- **Dependency injection**: [Hilt](https://developer.android.com/training/dependency-injection/hilt-android)
- **Asynchronous programming**: Kotlin Coroutines & Flow
- **Data storage**: Room database for local storage, with optional cloud sync in the future
- **Architecture pattern**: Clean Architecture with MVVM for the presentation layer

## Module structure

```
GlukoLab/
│
├── app/             # Main Android application module
├── core/            # Reusable utilities and base classes
├── data/            # Repositories and data sources (BLE, database, etc.)
├── domain/          # Business logic and use cases
└── presentation/    # Compose screens and view models
```

*Modules can be added gradually as the project evolves.*

## BLE communication

BLE communication with the Libre 2 sensor should be isolated in the `data` module. Use a repository pattern to expose sensor data as Kotlin `Flow` streams. This allows the rest of the app to remain agnostic of the BLE implementation.

## UI layer

Jetpack Compose enables a clean, declarative approach to building UI. Combine Compose with ViewModels from the `presentation` module to reactively update screens as data changes. Keep UI minimal and focused on current glucose values and trend charts.

## Testing

- Use JUnit and AndroidX Test for unit and instrumentation tests
- Prefer testable components in the `domain` and `data` modules
- Mock BLE and database layers during tests

## Future extensions

The architecture should allow future features such as A/B testing of meals, analytics, and cloud synchronization. By separating the app into clear modules and using dependency injection, new functionality can be added with minimal impact on existing code.


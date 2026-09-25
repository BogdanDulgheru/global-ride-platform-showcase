# Global Ride — Demo Walkthrough

This document describes the public product demo without exposing implementation details.

## Passenger journey

1. Open Global Ride and enter a destination.
2. Search suggestions resolve real places such as Vienna Airport.
3. The app calculates the route and presents Economy, Comfort and XL ride options.
4. The passenger selects a category and requests a ride.
5. The product enters driver-matching state.
6. After acceptance, the passenger can follow the ride lifecycle through pickup and trip completion.
7. The passenger can rate the experience and add a tip.
8. The demo payment flow closes the journey and produces a receipt.

## Driver journey

1. Driver goes online.
2. An incoming ride request presents the trip context and fare.
3. Driver accepts the request.
4. Driver proceeds to pickup.
5. Driver confirms passenger pickup and starts the ride.
6. The ride moves into an active state.
7. Driver completes the trip.

## What this proves

The demo shows a connected product workflow rather than isolated UI mockups: passenger and driver states, destination search, route calculation, ride categories, request/acceptance, pickup, trip lifecycle, feedback and demo payment/receipt flow.

## What it does not claim

This prototype does not claim production scale, live marketplace liquidity, production payment processing, regulatory launch readiness or proven commercial traction.

## What stays private

The public demo intentionally excludes source code, credentials, internal API implementation, detailed pricing mechanics, proprietary business rules and the private unit-economics model.

# Mr Banker EA

This is the readme file for the Mr Banker EA code. The Mr Banker EA is a forex trading robot developed by the Forex Robot Easy team. For detailed reviews and trading results of this product, you can visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/mr-banker-forex-software-review-proven-strategy-with-low-drawdown/). Please note that Forex Robot Easy is not the official developer of this product. We only provide a sample code that can work as described in this product. To find the official developer of this product, please use MQL5.

## Table of Contents

- [Introduction](#introduction)
- [Input Parameters](#input-parameters)
- [Initialization](#initialization)
- [Tick Function](#tick-function)
- [Deinitialization](#deinitialization)

## Introduction

The Mr Banker EA is designed to trade in the forex market during the New York trading session. It uses a strategy called Gopher I to determine the entry level and implements an advanced price movement strategy to calculate support and resistance levels. The EA opens pending buy and sell orders at the support and resistance levels respectively.

## Input Parameters

The following input parameters can be customized:

- `OrderExpiration`: Time in minutes for pending order expiration.
- `LotSize`: Size of the trading lot.
- `StopLoss`: Stop loss in pips.
- `TakeProfit`: Take profit in pips.

## Initialization

In the initialization function `OnInit()`, the New York trading session start and end times are set. If the current time is outside the New York trading session, the EA will print a message and return `INIT_FAILED`. Otherwise, the last order open time is set to the current time.

## Tick Function

In the tick function `OnTick()`, the EA first checks if a pending order is already open. If there is an open order, the function returns. Next, it checks if it's a new trading day by comparing the current time with the last order open time. If it's a new day, the EA proceeds to implement the Gopher I strategy to determine the entry level.

After calculating the support and resistance levels based on the advanced price movement strategy, the EA opens a pending buy order at the support level and a pending sell order at the resistance level. If the orders are successfully opened, the last order open time is updated. Otherwise, an error message is printed.

## Deinitialization

In the deinitialization function `OnDeinit()`, any necessary cleanup is performed before the EA is removed from the chart. A deinitialization message is printed.

Please note that this readme file only provides an overview of the Mr Banker EA code. For detailed reviews and trading results of this product, please visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/mr-banker-forex-software-review-proven-strategy-with-low-drawdown/).

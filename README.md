# markov-regime-dashboard
A real-time desktop trading dashboard that connects to Interactive Brokers (TWS/IB Gateway) to stream live market data and classify volatility regimes on the fly using a Hidden Markov Model. Built with Python, tkinter, and matplotlib, it visualizes live OHLC candlesticks color-coded by detected regime (Low / Medium / High volatility).

Features:

1. Live connection to Interactive Brokers via the ibapi client/wrapper
2. Real-time OHLC bar construction from streaming tick data (configurable bar duration)
3. Bayesian regime detection using a 3-state Markov chain (prior → likelihood → posterior updates each bar)
4. Historical data-driven calibration of emission means/stds and transition probabilities
5. Dark-themed live candlestick chart with regime-colored background shading
6. On-demand model recalibration while streaming
7. Live stats panel: bar count, high/low, current regime, ticks per bar
8. Responsive tkinter GUI with threaded data handling to keep the UI unblocked

Tech stack: Python, tkinter, matplotlib, numpy, ibapi (Interactive Brokers API), threading

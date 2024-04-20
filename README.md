# hedging-orders-executor

write down the mql4 code to execute hedging orders if any buy or sell position goes below -$5 then it will  open a opposite sell or buy positions And same thing will be continue to iterate in the for loop upto 10th buy or sell position. For ex. If the first open position is OP_BUY and it goes below -$5 then a first opposite hedging sell OP_SELL position will be opened and if this hedge position running profit is above $3 then it will open a limit trailling stop loss at $1, and if somehow this hedging sell position does't make running profit above $3 then open a stop loss limit order at -$5. This logic will further continue in for loop whenever next consecutive 2,3,4,5,6,7,8,9,10 positions showing loss of with increment of -5 ( for this we can use for lool - for(current_loss=0; current_loss>=-$34; current_loss-=3)), For this code i want user input variables as current_loss, minimum distance travel in USD which is running_profit of hedge position, trailling_H_SL when running_profit goes above $5 and H_stop_loss when running_profit is reverses back from <$5

## Collaborate with GPT Engineer

This is a [gptengineer.app](https://gptengineer.app)-synced repository 🌟🤖

Changes made via gptengineer.app will be committed to this repo.

If you clone this repo and push changes, you will have them reflected in the GPT Engineer UI.

## Tech stack

This project is built with React and Chakra UI.

- Vite
- React
- Chakra UI

## Setup

```sh
git clone https://github.com/GPT-Engineer-App/hedging-orders-executor.git
cd hedging-orders-executor
npm i
```

```sh
npm run dev
```

This will run a dev server with auto reloading and an instant preview.

## Requirements

- Node.js & npm - [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating)

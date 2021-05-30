# Codes
#Best Time to Buy and Sell Stock
You are given an array prices where prices[i] is the price of a given stock on the ith day.

You want to maximize your profit by choosing a single day to buy one stock and choosing a different day in the future to sell that stock.

Return the maximum profit you can achieve from this transaction. If you cannot achieve any profit, return 0.
//Solution

class Solution {
    public int maxProfit(int[] prices) {
      int n=prices.length;
        int i=1;
        int min=prices[0];
        int max_profit=0;
        while(i<n){
          if(prices[i]>min){
            max_profit=Math.max(max_profit,prices[i]-min);  
          }
            else{
                min=prices[i];
            }
            i++;
        }
        return max_profit;
    }
}

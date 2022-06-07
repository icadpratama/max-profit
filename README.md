import java.util.ArrayList;
import java.util.List;

public class MaxProfit {
    public static void main(String[] args) {
        List<Integer> prices = new ArrayList<>();

        if (prices.size() > 200000) {
            System.exit(0);
        }

        prices.add(23171);
        prices.add(21011);
        prices.add(21123);
        prices.add(21366);
        prices.add(21013);
        prices.add(21367);
        List<Integer> temp = new ArrayList<>();

        int currentProfit;

        for (int i = 0; i < prices.size(); i++) {
            for (int j = 1; j < prices.size(); j++) {
                currentProfit = prices.get(j) - prices.get(i);
                temp.add(currentProfit);
            }
        }

        int minValue = 0;

        for (Integer integer : temp) {
            if (minValue < integer) {
                minValue = integer;
            }
        }

        System.out.println(minValue);
    }
}

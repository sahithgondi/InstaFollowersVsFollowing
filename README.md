# InstaFollowersVsFollowing

code to check your following vs your followers on instagram
basically check who unfollowed you on insta

go to insta app, go to profile, go to settings, go to your activity, scroll down and click on 'download your information', press download some of your information, click followers and following, and then download it to your device. 
should get an email in a few minutes that lets you know to go back to the 'download your information page' open the file and copy the list of following and paste it into the console. enter the word 'end' and then do the same for followers. 
you can paste the entire thing so just leave the information that has the date and time on it



import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        List<String> following = new ArrayList<String>();
        List<String> followers = new ArrayList<String>();

        System.out.println("Enter names of your following. Type 'end' to end the list.");
        while (true) {
            String input = scanner.nextLine();
            if (input.equalsIgnoreCase("end")) {
                break;
            }
            following.add(input);
        }

        System.out.println("Enter names of your followers. Type 'end' to end the list.");
        while (true) {
            String input = scanner.nextLine();
            if (input.equalsIgnoreCase("end")) {
                break;
            }
            followers.add(input);
        }

        System.out.println("Names in following not in followers:");
        for (String name : nameCheck(following)) {
            if (!namesInList2.contains(name)) {
                System.out.println(name);
            }
        }

        scanner.close();
    }

    private static List<String> nameCheck(List<String> list) {
        List<String> finalList = new ArrayList<String>();
        for (String item : list) {
            if (!item.contains(",")) {
                finalList.add(item);
            }
        }
        return finalList;
    }
}

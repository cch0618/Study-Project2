import java.util.Arrays;
 
class Solution {
    public int[] solution(int[] array, int[][] commands) {
        int length = commands.length;
        int[] answer = new int[length];
        for(int i=0; i<length; i++)
        {
            
            int m = commands[i][0]; //앞
            int n = commands[i][1]; //뒤
            int k = commands[i][2]; //찾는숫자
            
            int temp[] = new int[n-m+1];//앞,뒤 자른거 temp배열에 저장
            int a = 0;//변수생성
            //배열 크기
            for(int j=m-1; j<n; j++)
            {
                temp[a++] = array[j];
            }
            Arrays.sort(temp);
            answer[i] = temp[k-1];
        }
        
return answer;
    }
}

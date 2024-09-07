class Solution {
    public void gameOfLife(int[][] board) {
        int m=board.length;
        int n=board[0].length;
        int[][] mat=new int[m][n];
        for(int i=0;i<m;i++){
            for(int j=0;j<n;j++){
                mat[i][j]=board[i][j];
            }
        }
        for(int i=0;i<m;i++){
            for(int j=0;j<n;j++){
                board[i][j]=sol(mat,i,j);
            }
        }
    }
    public int sol(int[][] mat,int r,int c){
        int count=0;
        count+=value(mat,r+1,c);
        count+=value(mat,r,c+1);
        count+=value(mat,r-1,c);
        count+=value(mat,r,c-1);
        count+=value(mat,r+1,c+1);
        count+=value(mat,r-1,c-1);
        count+=value(mat,r+1,c-1);
        count+=value(mat,r-1,c+1);
        if(mat[r][c]==0){
            if(count==3) return 1;
            return 0;
        }else{
            if(count<2) return 0;
            if(count>3) return 0;
            return 1;
        }
    }
    public int value(int[][] mat,int r,int c){
        if(r<0 || c<0 || r>=mat.length || c>=mat[0].length) return 0;
        if(mat[r][c]==0) return 0;
        return 1;
    }
}

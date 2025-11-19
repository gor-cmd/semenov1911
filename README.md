    1  sudo apt update
    2  sudo apt install -y apt-transport-https ca-certificates curl gnupg
    3  sudo install -m 0755 -d /etc/apt/keyrings
    4  sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
    5  sudo chmod a+r /etc/apt/keyrings/docker.asc
    6  echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
$(. /etc/os-release && echo "$UBUNTU_CODENAME") stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
    7  sudo apt update
    8  sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y
    9  sudo docker version
   10  sudo systemctl status docker
   11  mkdir semenov1911
   12  cd semenov1911/
   13  git init
   14  git remote add origin git@github.com:gor-cmd/semenov1911.git
   15  git branch -M main
   16  git push -u origin main
   17  echo "commit 1" > text.txt
   18  git add text.txt
   19  git commit -m "initial commit"
   20  echo "commit 2" > text.txt
   21  git commit -m "2 commit"
   22  git add text.txt
   23  git commit -m "2 commit"
   24  git commit -m "3 commit"
   25  echo "commit 3" > text.txt
   26  git commit -m "3 commit"
   27  git add .
   28  git commit -m "3 commit"
   29  echo "commit 4" > text.txt
   30  git add .
   31  git commit -m "4 commit"
   32  git push
   33  git remote add origin git@github.com:gor-cmd/semenov1911.git
   34  git branch -M main
   35  git push -u origin main
   36  git push
   37  git log --oneline
   38  git checkout 1030999
   39* git checkout dev
   40  git checkout -b test
   41  git push
   42  git push -u origin dev
   43  git push -u origin test
   44  git checkout dev
   45  git add copybara.svg
   46  ls
   47  git add capybara.svg
   48  git commit -m "add capybara"
   49  nano capybara.svg 
   50  git add capybara.svg
   51  git commit -m "change backcolor capybara"
   52  nano capybara.svg 
   53  git add capybara.svg
   54  git commit -m "change color capybara"
   55  git push
   56  git branch
   57  git checkout test
   58  git cherry-pick 1030999
   59  git cherry-pick 2354203
   60  nano text.txt 
   61  git cherry-pick --continue
   62  nano text.txt 
   63  git cherry-pick --continue
   64  git add .
   65  git cherry-pick --continue
   66  git cherry-pick 1f467bf
   67  nano text.txt 
   68  git add .
   69  git cherry-pick --continue
   70  git push origin test
   71  git checkout main
   72  git merge test
   73  nano text.txt 
   74  git merge --continue
   75  git add .
   76  git merge --continue
   77  git push origin main
   78  git checkout dev
   79  git rebase main
   80  git add .
   81  git push
   82  git push --force-with-lease origin
   83  history > README.md

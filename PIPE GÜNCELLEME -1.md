# PIPE GÜNCELLEME -1

## Dede ile ilk önce dashboard'dan güncelleme linkimizi alalım. Komutun çıktısındaki url'yi kopyalayın bi kenara.

```bash
cd $HOME
sudo systemctl stop popd
cd $HOME/pipe && ./pop --status
```

## Sonra kuruluma geçelim

```bash
cd $HOME
wget linki-yaz
chmod +x ./pop
rm -rf $HOME/pipe/pop
mv $HOME/pop $HOME/pipe/pop
cd $HOME/pipe && ./pop --refresh
```

## En son kontrol edelim

```bash
./pop --status
```

## Bi de restart atalım

```bash
sudo systemctl restart popd
```

## Logu kontrol edelim

```bash
sudo journalctl -u popd -fo cat --since "1 hour ago"
```

Tamamlandı!

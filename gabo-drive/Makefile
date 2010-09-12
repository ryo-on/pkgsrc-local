# $NetBSD$
#

DISTNAME=	Gabo___Free_Elegant_Font_by_Dannci.otf
PKGNAME=	gabo-drive-1
CATEGORIES=	fonts
MASTER_SITES=	http://www.deviantart.com/download/157988169/
EXTRACT_SUFX=	# empty

MAINTAINER=	ryo_on@yk.rim.or.jp
HOMEPAGE=	http://typethefont.com/post/463554113/gabo-drive-free-font
COMMENT=	Gabo Drive is new ultra-bold sans serif free font
LICENSE=	open-font-license

PKG_DESTDIR_SUPPORT=	user-destdir

USE_X11BASE=	yes
NO_CONFIGURE=	yes
NO_BUILD=	yes

INSTALLATION_DIRS=	lib/X11/fonts/TTF

FONTDIR=	${PREFIX}/lib/X11/fonts/TTF
FONTS_DIRS.ttf=	${FONTDIR}

INSTALL_FONTS=	${DISTNAME}

USE_LANGUAGES=	# none

WRKSRC=	${WRKDIR}

do-install:
.for fontfile in ${INSTALL_FONTS}
	${INSTALL_DATA} ${WRKSRC}/${fontfile} ${DESTDIR}${FONTDIR}
.endfor
.for docfile in ${INSTALL_DOCS}
	${INSTALL_DATA} ${WRKSRC}/${docfile} ${DESTDIR}${DOCSDIR}
.endfor

.include "../../mk/bsd.pkg.mk"

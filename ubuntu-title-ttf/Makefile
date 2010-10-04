# $NetBSD$
#

DISTNAME=	ttf-ubuntu-title_0.20080108.orig
PKGNAME=	${DISTNAME:S/_0./-/:S/ttf-//:S/.orig//}
CATEGORIES=	fonts
MASTER_SITES=	http://ftp.debian.org/debian/pool/main/t/ttf-ubuntu-title/

MAINTAINER=	ryo_on@yk.rim.or.jp
HOMEPAGE=	https://wiki.ubuntu.com/UbuntuTitle
COMMENT=	Logo font used by Ubuntu from 2004-2010
LICENSE=	gnu-lgpl-v3

PKG_DESTDIR_SUPPORT=	user-destdir

USE_X11BASE=	yes
NO_CONFIGURE=	yes
NO_BUILD=	yes

INSTALLATION_DIRS=	lib/X11/fonts/TTF

FONTDIR=	${PREFIX}/lib/X11/fonts/TTF
FONTS_DIRS.ttf=	${FONTDIR}

INSTALL_FONTS=	UbuntuTitling-Bold.ttf

USE_LANGUAGES=	# none

#WRKSRC=	ttf-ubuntu-title-0.20080108
WRKSRC=	${WRKDIR}/${DISTNAME:S/_/-/:S/.orig//}

do-install:
.for fontfile in ${INSTALL_FONTS}
	${INSTALL_DATA} ${WRKSRC}/${fontfile} ${DESTDIR}${FONTDIR}
.endfor

.include "../../mk/bsd.pkg.mk"
